# 2016 MCM Problem C: The Goodgrant Challenge


The Goodgrant Foundation is a charitable organization that wants to help improve educational performance of undergraduates attending colleges and universities in the United States. To do this, the foundation intends to donate a total of $100,000,000 (US100 million) to an appropriate group of schools per year, for five years, starting July 2016. In doing so, they do not want to duplicate the investments and focus of other large grant organizations such as the Gates Foundation and Lumina Foundation.

Your team has been asked by the Goodgrant Foundation to develop a model to determine an optimal investment strategy that identifies the schools, the investment amount per school, the return on that investment, and the time duration that the organization’s money should be provided to have the highest likelihood of producing a strong positive effect on student performance. This strategy should contain a 1 to N optimized and prioritized candidate list of schools you are recommending for investment based on each candidate school’s demonstrated potential for effective use of private funding, and an estimated return on investment (ROI) defined in a manner appropriate for a charitable organization such as the Goodgrant Foundation.

To assist your effort, the attached data file (ProblemCDATA.zip) contains information extracted from the U.S. National Center on Education Statistics (www.nces.ed.gov/ipeds), which maintains an extensive database of survey information on nearly all post-secondary colleges and universities in the United States, and the College Scorecard data set (https://collegescorecard.ed.gov) which contains various institutional performance data. Your model and subsequent strategy must be based on some meaningful and defendable subset of these two data sets.

In addition to the required one-page summary for your MCM submission, your report must include a letter to the Chief Financial Officer (CFO) of the Goodgrant Foundation, Mr. Alpha Chiang, that describes the optimal investment strategy, your modeling approach and major results, and a brief discussion of your proposed concept of a return-on-investment (ROI) that the Goodgrant Foundation should adopt for assessing the 2016 donation(s) and future philanthropic educational investments within the United States. This letter should be no more than two pages in length.


The ProblemCDATA.zip data file contains:

* Problem C - IPEDS UID for Potential Candidate Schools.xlsx
* Problem C - Most Recent Cohorts Data (Scorecard Elements).xlsx
* Problem C - CollegeScorecardDataDictionary-09-08-2015.xlsx
* IPEDS Variables for Data Selection.pdf


---
## Contents

* [2016 MCM Problem C: The Goodgrant Challenge](#2016-mcm-problem-c-the-goodgrant-challenge)
  * [Contents](#contents)
  * [An Educational Donation Mechanism Based On Data Insight(Team \#50193)](#an-educational-donation-mechanism-based-on-data-insightteam-50193)
    * [Summary](#summary)
    * [Introduction](#introduction)
    * [Data Processing](#data-processing)
    * [ROI Evaluation](#roi-evaluation)
    * [Model Construction](#model-construction)
    * [Sensitive analysis and validation](#sensitive-analysis-and-validation)
    * [Future Work(Gao)](#future-workgao)
    * [Conclusion](#conclusion)
    * [News Release(Gao)](#news-releasegao)
  * [The Optimal Investment Strategy Based on the Large\-\-scale Non\-linear Constraint Optimization Methods (Team \#47823)](#the-optimal-investment-strategy-based-on-the-large--scale-non-linear-constraint-optimization-methods-team-47823)
    * [Summary(Gao)](#summarygao)
    * [Problem Statement(Gao)](#problem-statementgao)
    * [Assumptions(Liu)](#assumptionsliu-1)
    * [Data Analysis and Focus Decision(Liu)](#data-analysis-and-focus-decisionliu)
    * [School Selecting(Liu)](#school-selectingliu)
    * [Strategy Making(Liu)](#strategy-makingliu)
    * [Result(Hu)](#resulthu)
    * [Test our model(Hu)](#test-our-modelhu)
    * [Conclusion(Hu)](#conclusionhu)
    * [Letters to the CFO(Gao)](#letters-to-the-cfogao)
  * [An Optimal Strategy of Donation for Educational Purpose (Team \#42939)](#an-optimal-strategy-of-donation-for-educational-purpose-team-42939)
    * [Summary(Gao)](#summarygao-1)
    * [Introduction(Gao)](#introductiongao)
    * [Addressing the Missing Values(Liu)](#addressing-the-missing-valuesliu)
    * [Determining the Performance Index(Liu)](#determining-the-performance-indexliu)
    * [Identifying Performance Contributing Variables via Post\-LASSO(Liu)](#identifying-performance-contributing-variables-via-post-lassoliu)
    * [Determining Investment Strategy based on ROI(Liu)](#determining-investment-strategy-based-on-roiliu)
    * [Extended Model(Hu)](#extended-modelhu)
    * [Conclusions and Discussion(Hu)](#conclusions-and-discussionhu)
    * [Letters to the CFO(Gao)](#letters-to-the-cfogao-1)
  * [A Multilevel Bayesian Model based on Economic Contribution of University Alumni (Team \#52815)](#a-multilevel-bayesian-model-based-on-economic-contribution-of-university-alumni-team-52815)
    * [Summary(Gao)](#summarygao-2)
    * [Introduction(Gao)](#introductiongao-1)
    * [Data Cleaning and Imputation Schema(Liu)](#data-cleaning-and-imputation-schemaliu)
    * [Model Components(Liu)](#model-componentsliu)
    * [Solving the Optimization Problem(Hu)](#solving-the-optimization-problemhu)
    * [Problem Statement and Special Considerations(Liu)](#problem-statement-and-special-considerationsliu)
    * [Model Analysis(Hu)](#model-analysishu)
    * [Results from Model(Hu)](#results-from-modelhu)
    * [Conclusion(Hu)](#conclusionhu-1)
    * [Letters to the CFO(Gao)](#letters-to-the-cfogao-2)

---

## An Educational Donation Mechanism Based On Data Insight(Team #50193)

### Summary

* **Introduction**
    * Background
    * Combine our own paper
* **Operate on the data**
    * Data screening
    * Deleting data
    * merging attributes
    * Missing data imputation
    * Normalize data
* **Construct a ROI evaluation critria**
    * **Propose the model**
        * Ratio: output/input
        * Coefficient: urgency
    * **Explain the significance of model parameters**
        * The ratio reflects the benefits in related to the cost
        * Urgency reflacts the demand of money
    * **Explain how to set model parameters**
        * PCA
        * AHP
* **Put forward two kinds of model:**
    On the basis of ROI, the concept of risk ( Imitating the concept of Modern Portfolio Theory) is introduced.
    * **Basic model for one year**
        * Mixed Integer Linear Programming Algorithm
    * **Time series for five year**
        * MILP
        * Grey Prediction
* **Make sensitivity analysis**
    * the amount of schools
    * the restriction for money
    * whether allocating the money equally or not
* **To sum up**
    * Feasible
    * Reasonable
    * **Subjectivity**

### Introduction

#### Background(Gao)

* Explain why data is needed to guide work and life.
* Explain why this model needs ROI.
* A brief explanation of our work and the theory we used。

#### Overview of Our Work(Gao)

* Decompose the whole problem into small issues
* Divide our task into small steps

#### Assumptions(Liu)
* 1.忽略通货膨胀和通货紧缩，认为钱的价值保持不变。
* 2.题目的目的是为了提高教学水平以及社会贡献，不是为了获利
* 3.我们的奖学金不是为了奖励在某些方面有特殊贡献的人
* 4.如果和别的慈善组织有不同的目标和策略，我们的方案会节约一大部分成本。
* 5.我们只负责选学校，不考虑个人的问题。给谁发放是学校的问题。
* 6.我们的模型只考虑我们策略的公平性，不考虑学校的声誉
* 7.因为边际效用，我们不会给一个学校投资很多钱
* 8.在只考虑时间的模型中，我们忽略掉不包括在模型外的因素。也就是说，未来可以预测。

### Data Processing

#### Data Screening(Liu)
* 1.删掉经济状况不好以及缺乏学生信息的学校，删掉有一半以上特征为NULL的学校。总共选取了7805个学校。
* 2.将一些具有二重性的特征结合成为一个特征。将一些有缺失值的特征进行补值。保留了一些比较特殊的学校，像什么什么女子大学，为了后面聚类和补值的需要。
我们删掉地址、学生年龄等对ROI计算无用的信息。


#### Data imputation(Liu)
* 1.用K-means聚类方法来进行聚类,K值是用R^2 statistic来确定的。
* 2.一些变量是对ROI有影响但是缺失值，有一些是完整的，可以通过完整的值来指导填值。通过这些变量可以很好来分辨学校的相同和不同。
* 3.只对完整的数据进行K-means聚类，认为这些完整的数据的聚类同样适用于那些不完整的数据。最合适的K值为5.我们认为在同一class的学校具有最大的相似性。
#### Data Normaliztion(Liu)
用最大最小值来进行数据的归一化：x'=(x-xmin)/(xmax-xmin)
### ROI Evaluation
* ROI是用来衡量金融投资的一个指标 ：ROI=(Output/Input)Urgency
* 输出主要是用来衡量教育的一个指标，Output={V1*[SAG RR RA EER]T
                                      V2*[SAG RR RA]T  }
* 衡量输出用到的数据有四个SAG（毕业后的薪资） RR（保留率） RA（偿还能力） EER（教育提高率）；V1 V2是权重。
* INPUT=（1-a）+a NP                                            
* a是修正指数，因为NP是输入中仅有的一个指标，所以他影响很大要加修正指数a
因为我们是给一个慈善组织做进行相关的评定，所以要给ROI修正，Urgency是一个修正指数，用来修正ROI。
* Urgency=V3 [PG FL DEBT]T
* V1 V2是通过层次分析法获得的，V3是通过主成分分析法获得的。
#### Using Grey Theory to Predict ROI(Liu)
灰度预测主要是用到了GM(1,1)模型，它是基于随机的原始时间序列，经按时间累加后所形成的新的时间序列呈现的规律可用一阶线性微分方程的解来逼近。经证明，经一阶线性微分方程的解逼近所揭示的原始时间序列呈指数变化规律。因此，当原始时间序列隐含着指数变化规律时，灰色模型GM(1,1)的预测结果会很好。
这个模型是用来预测未来五年的数据的。
### Model Construction
在基础模型，忽视掉时间因素，并且假设资金是在很短时间内发完。用一个连续变量来代表学校收到的资金支持，用一个二元的变量来代表学校是否收到资助。
在复杂模型中要考虑到时间。
最终会给出在两个模型下的结果。

#### Definition of Risk(Liu)
risk是一个特征的标准差比上平均值
#### Basic Model(Liu)
1.为了获得最大的回报，要找到最大的ROI
2.投资有范围限制
3.资助的学校数量也有范围
4.学校的规模太小就不予考虑
#### Results of Basic Model(Hu)

* **假设**
    * 最低学生人数Smin=1000
    * 最低学校投资A(i)min=20000000
    * 最高学校投资A(i)max=A(i)min+b*s(i)，b=3000，s(i)为学校i的学生数
    * 最大投资学校数Nmax=30，最小投资学校数Nmin=10
    * 忽略风险，只追求最高回报

* **解决方法**
    * ILOG CPLEX（解决规划问题）
    
* **结果**
    * 图1 表格 需要填补数据的学校
    * 图2 柱状图 各学校ROI数据
    * 图3 饼图 投资分配策略（基础模型仿真结果）

#### Time Series Model(Liu)
因为投资是要考虑到对五年的投资，所以还要在变量中加入t这一影响。t代表年，以年为单位。

#### Results of Time Series Model(Hu)

* **假设**
    * 最低学校投资A(i)min=5000000
    * 最高学校投资A(i)max=A(i)min+b*s(i)，b=8000，s(i)为学校i的学生数
    * ？可接受最大风险rmax未给出

* **解决方法**
    * ILOG CPLEX（解决规划问题）
    
* **结果**
    * 表格 未来5年投资分配策略

### Sensitive analysis and validation

#### Risk-Return(Hu)

* **改变量 可接受最大风险（0.2-1）**

* **图 最大收益随可接受最大风险的变化**

* **结论**
    初始时，最大收益随可接受最大风险的增加而增加，当可接受最大风险达到0.82后，最大收益不再增加。

#### School Number(Hu)

* **改变量 选择学校的数量**

* **图 最大收益随选择学校的数量的变化**

* **结论：**
    初始时，最大收益随选择学校的数量增加而陡升，然后达到12所左右时最高，随后开始逐渐下降。

#### Policy of Distribution(Hu)

* **改变量 资金分配策略**
    1. 所有资金都在第一年投资
    2. 5年内资金平均分配，每年200000000
    3. 5年内资金不平均分配，但每年投资额有最大值和最小值限制
    4. 无限制分配

* **表格 四种分配策略下的最大收益和gap（投资空白率）**

* **结论：**
    策略4的最大收益最高但不符合实际，策略3投资gap只有3.5%，避开了极端情况，说明模型是经得起检验的。

### Future Work(Gao)

**We cannot figure out intuitively why we should invest them**

* Invite experts to do the subjective evaluation.
* Focus on differen subjects and different students.
* More data is needed.
    * More data of missing data.
    * More data of information of schools.
    * More data of other charitable organization.


### Conclusion

#### Strengths(Hu)

* **完整性：**
使用了所有数据，考虑了时间序列。

* **科学理论支撑：**
模型中使用了许多合理的科学理论和方法。

* **交叉融合性：**
使用金融领域的知识解决建模问题。

* **灵活可扩展：**
可以根据主观需要扩展模型适应更多情景。

#### weaknesses(Hu)

* **缺乏数据支持：**
需要更大量的数据来完善模型。

* **过于主观：**
模型中的一些方法过于主观，一些指数是由经验和直觉得出，不够可靠。

* **简化的假设：**
为使模型可求解，简化了假设，一些有价值的数据和信息没有用上。

* **忽略了未来动态：**
根据过去的数据预测了学校未来的变化，但是忽视了每年投资后会对学校产生的影响。

### News Release(Gao)

1. First is the opening remarks.
2. Point out what we want to do is to improve educational performance.
3. Firstly, the measure of the performamce in universities should be clarified.
    * Point out that Economic foundations of school is important.
    * Point out that evaluating the quality of the graduates is also important.
4. Introduce our formula：ROI
    * OUTPUT
    * INPUT
    * URGENCY
5. Make a summary of the formula.
6. Introduce the methods used in modeling and the outline of models we build.
7. Give the final result: the list of schools we chose.
8. Wish our model can help you at the key point of choosing the targets of donation.

---

## The Optimal Investment Strategy Based on the Large--scale Non-linear Constraint Optimization Methods (Team #47823)

### Summary(Gao)

* **Charitable identity**
Then we set out to decide our focus, which is to invest more on those schools with more minority races, lower educational performance, higher debt ratio and so on.

* **Data extraction: PCA**

* **Modeling**
    * **Key assumption**
        Social utility has logarithmic relationship with the earnings of graduated students and graduation rate.
    * **Hyperparameter K**
        Denote the marginal rate of substitution between the earnings of graduated students and graduation rate.
        两种商品之间的替代程度可以由商品的边际替代率来衡量。一种商品对另外一种商品的边际替代率定义为：在效用满足程度保持不变的条件下，消费者增加一单位一种商品的消费可以代替的另一种商品的消费数量，简称为边际替代率。
    * **ROI**
        Define the ROI function of each target school as the incremental utility.

* **Devise strategy**
    * **Improved PSO Algorithm Based on the Augmented Lagrange 基于增广拉格朗日的粒子群优化算法**
    A typical method to solve the multivariable optimization problem.
* **Make sensitivity analysis**
    * Parameter K

### Problem Statement(Gao)
We must set big goals and spare no effort on the way because the world won't get better by itself.

### Planned Approach(Gao)

* **Targets**
 * Target school
 * The investment amount per school.
 * The investment duration
* **Procedures**
 * Part One: Data Analysis and Focus Decision
      * Decide not to duplicating the investment and focus of other large grand organizations.
 * Part Two: School Selecting  
      * Manual selection
      * PCA
 * Part Three: Strategy Making
      * ROI
      * Optimization algorithm


### Assumptions(Liu)
1.五年内学校的数量是一个常数
2.学校会将所有的资金用于提高学生
3.效用函数必须是凹的
4.不考虑通货膨胀和通货紧缩
### Data Analysis and Focus Decision(Liu)
Data Analysis:
数据总共有两种：离散的和连续的
连续的数据可以分为两个组，一个组是用来决定学校选择的，另一个组是来衡量学校的效用函数以及ROI。
最后将所有的数据分为了三个部分：连续数据来选择学校、离散数据来选择学校、连续数据计算ROI
Focus Decision:
首先，认为这个慈善组织是为了让世界更公平。
其次为了不和其他慈善组织有一样的投资，我们勉强只考虑资金支持。
不投资纽约、加州、哥伦比亚地区、马萨诸塞州。
总结来说，目标如下
1.成绩低的
2.获得助学金比例低的地区
3.大比例少数民族的
4.每周项目受奖多的
5.时间比例？
6.贷款比例高的
### School Selecting(Liu)
1.人为删除（那四个州）
2.主成分分析法选择学校
   先将残缺的数据通过均值进行填补，然后对数据进行标准化处理。
   用处理完的数据进行协方差计算，获得协方差的特征值和特征向量。
   然后可以计算获得贡献率。
   贡献率的和越大，T越大，score越大。
   最后可以用score来rank school
### Strategy Making(Liu)
为了决定选择哪个学校进行投资，要使用ROI，在使用ROI先构建了一个效用函数U
U=log（x），x是输入（four main factors , student number , graduated ratio , earnings of graduated students and investment）
前提：U是一个凸函数，U是一个状态值。
### Result(Hu)

* **fitness figure 算法经过50次迭代后收敛，说明了算法的有效性**

* **Table 推荐列表前十的学校和每年的投资额**

有两个学校也在PCA结果的前十中，证明了数据的相关性。

### Test our model(Hu)

* **Table Gates Foundation投资前十的学校**

其他基金会关注的学校没有出现在我们的推荐列表中，证明我们的模型有效避开了其他基金会的关注点。

#### Sensitivity Analysis

* **改变K值（平均收入和平均毕业率的边际替代率）**
* **表 不同K值变化下，投资额的变化情况**
结论：K值的影响并不是很大，在我们可以忍受的范围内。


#### Strengths

* **数据分类：**
面对大量数据，把数据分类为两部分，一部分用于选择学校，一部分用于计算ROI。

* **数据提取：**
使用PCA方法基于我们的关注点选择目标学校。

* **合理的ROI函数：**
ROI函数综合考虑了收入和毕业率，并且两者之间如果有精确关系，函数可以很容易被修改。


* **算法：**
尝试了多种算法，选了最合适的一个。

#### Weaknesses

* **数据空缺：**
有许多空缺的数据用平均值填补的。

* **参数无数据参考：**
K值没有数据供参考，会影响ROI的输出。

* **算法的局限：**
粒子群算法的局部搜索能力不强，输出的精度不高；算法也有可能在找出最优点前过早收敛。

### Conclusion(Hu)

* 首先，确定慈善意义的重点，我们试图在那些少数族裔较多、SAT分数较低、负债率较高等学校投入更多。我们希望帮助那些表现不佳的学校，因为它们最有可能对学生的表现产生强烈的积极影响。

* 然后，使用数据分类、数据选择作为预处理，根据我们关注的关键指标，通过PCA选择目标学校。

* 确定一个估计的ROI函数，根据收入和毕业率量化收到我们投资的学校的增量效用。

* 使用机器学习算法，是目标学校五年的总ROI最优，输出结果，计算出每所学校每年的投资额。

* 结果，投资的学校并不是其他基金会投资的著名高校，这与预期相符。

### Letters to the CFO(Gao)

1. First is the opening remarks.
2. Point out what we want to do first is to decide the focus of the foundation.
3. The most creative work is that we determine a reasonableROI function based on the social utility.
    * More students the school has, the higher contributions school make.
    * The higher the earnings the graduated students are, the higher the utility is.
    * A higher utility school has high graduation rate.
4. Another point is that the utility function is concave(凹函数).
5. Another accomplishment is that we utilize a complex algorithm to maximize the total ROI of the target schools.
6. None of our target school is well-known, which is consistent with our focus.
7. We cling to the belief that our model is a powerful tool to help you devise the best investment strategy.

---

## An Optimal Strategy of Donation for Educational Purpose (Team #42939)

### Summary(Gao)

* **Start**

In order to determine the optimal donation strategy, this paper proposes a datamotivated model based on an original definition of return on investment (ROI) appropriate for charitable organizations.

* **Process**

    * **Addressing missing data.**
    * **Develop a composite index, called the performance index, to quantify students’ educational performance.**
    * **Employ a linear model and a selection method called post-LASSO to select variables that statistically significantly affect the performance index and determine their effects (coefficients).**
        * insusceptible
            * tuition & fees in 2010 (insusceptible)
            * Carnegie High-Research-Activity classification (insusceptible)
        * homogenous and heterogenous
            * percentage of students who receive a Pell Grant
            * share of students who are part-time
            * student-to-faculty ratio
            * homogenous: is modeled as the change in fitted values of performance contributing variables over increase in donation amount, which can be predicted from the fitted curve.
            * The heterogenous: is modeled as a tuning parameter which adjusts the homogenous influence based on deviation from the fitted curve.
    * **Calculate ROI**
    * **Also, we propose an extended model to handle problems caused by time duration and geographical distribution of donations.**

### Introduction(Gao)

* **Statement of the Problem**

    * There exists no doubt in the significance of postsecondary education to the development of society.
    * To achieve this goal, several large foundations like Gates Foundation and Lumina Foundation have developed different evaluation approaches...
    * In other empirical literature...
    * Make a conclusion about our work.

* **Baseline Model**

    * Our definition of ROI is similar to its usual meaning.
    * Cope with data missingness.
    * Then we divide the impact of donation amount into 2 parts: homogenous and heterogenous one. 
    * Calculate the ROI of the performance index.
    * Also, we propose an extended model to handle problems caused by time duration and geographical distribution of donations.

* **Assumptions(Liu)**

* **The Advantages of Our Model(Hu)**

### Addressing the Missing Values(Liu)
* 1.对于缺失大于50%的数据，省略
* 2.对于缺失（10%-50%）的数据，采用从相似记录随机取值填补的策略，基于模型分析的要用分配表中的数据替换&
* 3.对于缺失小于10%，采用均值填补的策略。

### Determining the Performance Index(Liu)
1.选择影响goodgrant concern 的因素，为了方便计算和解释，将所有的数据归一化
2.模型假设index是线性的，用PCF来对变量进行加权(PCA)
### Identifying Performance Contributing Variables via Post-LASSO(Liu)
LASSO是用来描述内在变量、表现指数以及对其有影响的变量的一个线性模型
给每个变量一个系数来减小均方误差。
但是因为很多变量在不断变化，所以引入post-LASSO模型来进行变量选择.。
如论文中所示，post-LASSO加入了一个惩罚因子。
利用LARS算法和最小二乘法，来获得最合适的惩罚因子。
共选出了六个变量。
### Determining Investment Strategy based on ROI(Liu)
* 选出的变量有几个对于投资金额不敏感，所以我们只考虑投资金额上升后对三个变量的影响，还有他们的系数。
将变量和投资金额进行拟合，获得fROI。
虽然提高投资金额产生的影响是同质的，但是大学使用投资金额的方式是不一样的。同质的影响只受投资金额以及金额的增加影响，而不同质的影响因校而异。
为了衡量不同质的影响，引入了参数P，
* ROI=fROI P
* 1.现在对不同的学校都有一个ROI值，通过每个学校的ROI值来确定投资金额。
* 2.然后通过ROI值来判断哪些学校的潜力大，然后从大选到资金用完。
### Extended Model(Hu)

* **时间**
    * 场景1：
    每年根据上一年投资结果带入模型得出新一年的投资策略。
    * 场景2：
    将未资助的学校视为固定，对前一年资助的学校的相关变量进行改变后带入模型得出新的投资策略。
    
* **地理分布**
    
    保证公平性。方案一：分割地理区域，在一个区域内运用模型分配资金。方案二：当当单个地区投资的机构数量超过了预设，对该地区的ROI打折扣。

### Conclusions and Discussion(Hu)

* **优势**
    * 通过PCA制定了performance指数
    * 确定了三个主要performance contributing变量
    * 通过GAM拟合推导出了performance contributing变量和捐赠量的关系，来预测出了ROI
    * 选择院校和确定投资额由两步算法完成
    
* **劣势**
    * 没有时间序列数据
    * post-LASSO selection仅适用于简单的线性模型

### Letters to the CFO(Gao)


1. Our team has proposed a performance index quantifying the students’ educational performance of each institution and defined the return of investment (ROI) appropriately for 
charitable organization like Goodgrant Foundation. 
2. The composite performance index is developed after taking all the possible performance indicators into consideration
3. Adopt a variable selection method to find out performance contributing variables.
4. And we calculate ROI, defined as increase in the performance index over your donation amount.
5. In conclusion, our model successfully produced an investment strategy including a list of
target institutions and investment amount for each institution.
6. None of our target school is well-known, which is consistent with our focus.
7. We cling to the belief that our model is a powerful tool to help you devise the best investment strategy.

---

## A Multilevel Bayesian Model based on Economic Contribution of University Alumni (Team #52815)

### Summary(Gao)

* **Bayesian multi-stage model to maximize Return on Investment over five years**

* Model One: Be made to relate the distribution of students' majors at school to the expected number of jobs that school will add to the economy.

* Model Two: Be fit to gibe the relationship between jobs added to the economy and changed in real GDP.

* Model Three: Goodness rate is related to added GDP and median salary.

* Model Four: A linear regression model relating Goodness to a combination of the school's tuition and enrollment.

* Model Five: ROI

### Introduction(Gao)

* **Introduce** Solid investments will have a positive effect on overall student performance.
* **Background**  There are important returns to expanding higher education, especially in developed countries such as the United States.
* **Overview** Return on Investment was calculated as a function of the school’s ”goodness” and the school’s resources.

### Data Cleaning and Imputation Schema(Liu)
* 1.用PYTHON重新组织了数据，删掉了一些具有不合理数据的学校
* 2.然后用R的程序分析了数据的结构
* 3.缺失的数据主要为两种：MCAR MAR用两种办法处理
### Model Components(Liu)
总共有两种方式来衡量学校的贡献，一种为衡量毕业生的技能对社会需求的满足，另外一种为毕业生平均工资
先是给出了一个GOODNESS的计算方式，然后每一个学校有一个prior

### Solving the Optimization Problem(Hu)

* **最小等效的例子**
    
    两个学校竞争资金，A学校对投资额效用的系数为1，B学校的系数为0.2，投资A学校对其影响更大，应该多投资A。
    
* **方案**
    
    迭代算法，计算每个学校Goodness/Resource斜率，每次迭代，对增幅最大的学校进行投资，直至资金耗尽。

### Problem Statement and Special Considerations(Liu)
* 这篇文章的主要目的是使这一百万达到最大的效果
* 我们的模型是告诉这个慈善组织，怎样评估投资的影响，给哪些学校投资，每个学校给多少，每个学校期望值是多少
* 除了分数数据，还考虑了其他特征。公立学校、私立学校以及社区大学。
### Model Analysis(Hu)

* **为什么用贝叶斯**

首先，在贝叶斯模型中填补确实数据很正常；其次，贝叶斯可以考虑不确定性。

* **模型的缺陷**
    * 没有时间序列数据以及具体领域的失业率数据
    * 许多学校的资助数据都是估计出来的，可能与现实不符
    
* **模型的假设**
    * 大部分输入假设五年内保持不变
    * 各领域的失业率保持稳定
    * 假设未被注意到的预测数据不会丢失
    
* **模型的优势**
    * 模型的每一步都独立且易于理解
    * 变量的子集映射到GDP的变化可以理解为一种ROI
    * 贝叶斯可以处理不确定问题
    
* **模型的改进**
    * 线性回归模型变为动态线性模型
    * 更多相关数据来提高模型的准确性
    * 考虑更多因素，如大学的研究成果

### Results from Model(Hu)

两个表，表1限制了每个学校的最大投资额，表2是没有限制的情况。

### Conclusion(Hu)

在不受限制时，表中既有知名学校，也有不知名的学校，证明了模型的合理性，但是出现了一所学校的投资额过多的情况，所以改进了模型，添加了限制额。限制额为每所学校5000万美元，结果是增加了投资学校的数量，使得平均投资额降低。有限制的改进模型更好的保护了可能存在的潜在ROI，并且避免了对某所学校可能出现的不预见的情况。

### Letters to the CFO(Gao)

* **An outlook of our work**
This measurement was a function of what we called Goodness obtained by and
resources available to a given school. 
    * **Goodness** was assessed as a school’s contribution to the U.S. Gross Domestic Product (GDP). 
    * **Resources** were defined as a school’s annual income from tuition and external funds. This RoI was optimized by the model’s simulations.
    
* **Detail** 
    * A positive relationship was then found between the amount of jobs added and the change in GDP.
    * Computed an overall model by looking at the relationship between resources and goodness for all the schools on which we had data.
    * Using this first model as a starting point, we developed individual models for each school.
    * Estimated RoI over time.
    
* **Conclusion**
    * After optimizing RoI, 73 schools were given at least some sort of investment.
    
* **End**
    * The recommended investments output from the model optimize an acceptable metric for gauging the added value to the invested schools. Multiple models were compared to one another to arrive at a concluded model for the recommended investments. We are confident that this model will realize its full potential.
