# 2017 ICM Problem D: Optimizing the Passenger Throughput at an Airport Security Checkpoint


继2001年9月11日美国发生恐怖袭击事件后，全世界的机场安全状况得到显着改善。机场有安全检查站，在那里，乘客及其行李被检查爆炸物和其他危险物品。这些安全措施的目的是防止乘客劫持或摧毁飞机，并在旅行期间保持所有乘客的安全。然而，航空公司有既得利益，通过最小化他们在安全检查站排队等候并等待他们的航班的时间，为乘客保持积极的飞行体验。因此，在希望之间存在最大化安全性同时最小化对乘客的不便的张力。

在2016年，美国运输安全局（TSA）受到了对极长线路，特别是在芝加哥的奥黑尔国际机场的尖锐批评。在此公众关注之后，TSA投资对其检查点设备和程序进行了若干修改，并增加了在高度拥堵的机场中的人员配置。虽然这些修改在减少等待时间方面有一定的成功，但TSA在实施新措施和增加人员配置方面花费了多少成本尚不清楚。除了在O’Hare的问题，还有在其他机场，包括通常有短的等待时间的机场不明原因和不可预测的长线的事件。检查站线路的这种高差异对于乘客来说可能是极其耗时的，因为他们决定要尽早到达，因为可能延迟错过他们的预定航班之间。许多新闻文章，包括[1,2,3,4,5]，描述了与机场安全检查站相关的一些问题。

您的内部控制管理（ICM）团队已经与TSA签订合同，审查机场安全检查站和人员配置，以确定可能干扰乘客吞吐量的瓶颈。他们特别感兴趣的创意解决方案，既增加检查点吞吐量，减少等待时间的方差，同时保持相同的安全和安全标准。

美国机场安全检查点的当前流程如图1所示。

 + **区域A：**

     + 乘客随机到达检查站，并等待队列，直到安全人员可以检查他们的身份证明和登机文件。

 + **区域B：**

     + 然后乘客移动到打开的筛选线的后续队列;根据机场的预期活动水平，或多或少的线路可能开放。

     + 一旦乘客到达这个队列的前面，他们准备所有的物品用于X射线检查。乘客必须用液体去除鞋子，皮带，夹克，金属物体，电子产品和容器，将它们放置在单独的X射线箱中;笔记本电脑和一些医疗设备也需要从其袋中取出并放置在单独的容器中。

     + 他们的所有物品，包括包含上述物品的箱子，由传送带通过X光机移动，其中一些物品被标记，供安全人员（D区）进行额外的搜索或筛选。

     + 同时乘客通过毫米波扫描仪或金属探测器进行处理。

     + 未能通过此步骤的乘客接受安全官员（D区）的轻击检查。

 + **C区：**

     + 乘客然后前进到X射线扫描仪另一侧的传送带，收集他们的物品并离开检查站区域。

图1：TSA安全筛选过程的图示。

大约45％的乘客报名参加一个称为预检查信任旅行者的计划。这些乘客支付85美元，接受背景调查，并享受五年的独立筛选程序。尽管事实上更多的乘客使用预检查过程，但是每三条常规车道通常有一个预检查车道打开。预检查乘客和他们的行李经过相同的筛选过程，经过一些修改，以加快筛选。预检查乘客还必须移除扫描用的金属和电子物品以及任何液体，但不需要去除鞋子，皮带或灯罩;他们也不需要从他们的包里删除他们的电脑。

收集了关于乘客如何进行安全检查过程的每个步骤的数据。

**您的特定任务是：**

 + a.开发一个或多个模型，允许您通过安全检查点探索乘客流，并识别瓶颈。清楚地确定当前流程中存在哪些问题区域。

 + b.对当前流程开发两个或多个潜在修改，以提高旅客吞吐量并减少等待时间的差异。对这些更改进行建模，以演示修改如何影响流程。

 + c.众所周知，世界上不同的地方都有自己的文化规范，塑造了地方社会互动的规则。考虑这些文化规范如何影响你的模型。例如，美国人以深为尊重和优先考虑别人的个人空间而闻名，在别人的面前“切割，或者理解为剪切”当作是一种社会歧视。同时，瑞士人以集体效率为重点，中国人以优先个人效率而闻名。考虑文化差异如何影响乘客的过程通过检查点作为敏感性分析的方式。您应用于敏感性分析的文化差异可以基于真实的文化差异，或者您可以模拟与任何特定文化（例如，较慢的旅行者）无关的不同旅行者风格。安全系统如何以加快乘客吞吐量并减少差异的方式来适应这些差异？

 + d.根据您的模型为安全管理器提出政策和程序建议。这些策略可以是全球适用的，或者可以针对特定文化和/或旅行者类型来定制。

**除了开发和实施您的模型来解决这个问题，您的团队还应该验证您的模型，评估优势和弱点，并提出改进建议（未来工作）。**

References:

[1] http://www.wsj.com/articles/why-tsa-security-lines-arent-as-bad-as-youd-feared1469032116

[2] http://www.chicagotribune.com/news/ct-tsa-airport-security-lines-met-20160823-story.html

[3] http://www.cnn.com/2016/06/09/travel/tsa-security-line-wait-times-how-long/

[4] http://wgntv.com/2016/07/13/extremely-long-lines-reported-at-chicago-midwayairports-tsa-checkpoint/

[5] http://www.cnbc.com/2016/04/14/long-lines-and-missed-flights-fuel-criticism-of-tsascreening.html




---
## Contents


---
## Judges' Commentary

### Problem Overview(Gao)

* 建一个模型反映乘客流
* 识别目前模型瓶颈位置
* 提出并分析潜在的修正
* 敏感性分析基于乘客等
* 推荐可行的政策和程序

### Judges' Criteria

* 高级的综述和发现
* 一个模型：能够评估安检乘客流（比如识别瓶颈位置）
* 将提供的数据fit进模型中
* **一些**潜在的对系统的修正以及他们的影响
* 敏感性分析基于乘客特征的（例如文化，种族等）
* **一些**推荐，这些推荐要兼具：
    * 上文的分析
    * 客观的事实（例如可行性，预算，人事部门和空间限制等）

#### Exposition（阐述）

* 模型质量 > 表述
* 要很好的表述
* 对模型要：
    * 很好的解释
    * 很好地讨论简化的假设和预期的影响
    * 可视化
* 高级的Summary
    * 介绍问题
    * 总览模型与方法
    * 高亮重要发现

#### Modeling Approaches

* 首先要确定如何使用提供的数据（乘客到达和安检时间）
    * 大部分团队观察得出最可能的分布（泊松分布）之后基于此分布生成大量数据
    * 另外一些团队，认为泊松分布可能出现异常值，所以手动去除了异常值或者使用了三角分布（辛普森分布）

* 开始建模
    * 很多队伍用了Petri Nets
    * 还有很多用了Discrete Event Simulator（离散事件模拟器）
    * 还有agent-based model（代理人基模型），partial differential equations（偏微分方程式）,欧姆定律（电流，电阻，电压）
    * 有的队伍还探索了为什么会出现瓶颈，基于时间点和当时的航班数

* 探索可能的提升和乘客的不同的影响
    *  现实生活中的改变如何体现在模型中
    *  可能的提升
      * 模拟了限制条件
      * 通过预检查做优化
    *  乘客不同的影响
      * 文化差异：是否接受插队等
      * 用户画像：怀疑型乘客，商务乘客，墨迹乘客 

* 推荐
    *  评委会考虑你的推荐是否被你的文章所支持
    *  好的推荐需要考虑到限制如成本，人力资源等
    *  还有些推荐能够考虑到人的因素，例如虚拟队伍（解放乘客去购物）
* 推荐可行的政策和程序改进

### Discussion of Outstanding Papers

#### 上海交大（1）(Gao)

#### 上海交大（2）(Liu)
* 他们在模型中添加了一个链接，表示增加了一个行李准备集结区，其中几个乘客可以一次准备好他们的物品，谁先整理好就可以前进，为其他人准备物品腾出空间。
* 他们修改了排队算法，增加了一条应急车道，以容纳有误飞风险的乘客，包括迟到的乘客和已经排队一段时间但现在有误飞风险的乘客。
* 该小组修改了该模型，将老人和儿童视为预检查，因为TSA通过了一项规则，不要求这些乘客脱鞋或轻夹克。 
#### NC School(Hu)

* 乘客独自出行的假设
* 根据数据计算出了每一秒乘客出现的概率、为搜身和行李搜查分配了概率
* 不同的出现概率、不同的配置模拟各种情况
* 六种不同情况的改进模型
* 增加设备和人力，没有考虑费用问题

#### Brown University(Liu)

#### 浙大(Hu)
* 验证了检查者的服务差异没有显著影响

### Conclusion(Gao)

---


## Analsis and Optimization to the Process od Aieport Security Check(Team #55285)上海交大（2）

### Summary(Gao)

 - 等待时间长，等待时间不确定，我们做了一些修正
 - 基础模型：模拟了现状，研究了pre-check
 - 两个有效的修正模型：
     - multi-passenger linkage model of belongings preparation
     - priority-based queuing model
 - 考虑中国人的情况建立模型：cut-in-line model

### Restatement of the Problem(Gao)

 1. 背景
     - 问题回顾
         - 出事儿了，安检变严了，问题出现了
         - 问题本质：队伍过长和长度变化大
     - 安检流程
         - 开始
         - 等待安检
         - 身份核查
         - 等待扫描
         - 脱衣
         - 扫描
         - 可能的额外检查
 3. 文献综述：将题目给的五篇论文总结
 4. 任务：建模，修正模型，考虑差异，提供推荐

### Assumptions and Notations(Liu)
* excel中的数据在某种程度上可以表现出所有的情况。我们用不同的方法计算出在不同进程中时间消耗的均值和标准差。
* 乘客到达的时间间隔符合Poisson 分布。
* ID检查和毫米波扫描时间符合高斯分布。
* 两个检查的X光扫描时间间隔为11s,一个检查需要花费2s。
* 所有的乘客都会遵守规矩（没有人插队）。
* 机场里不会发生紧急事件。
* Pre-check 乘客也可以选择普通通道。
* 在Pre-check通道，准备时间为15+-5+5Xs，正常通道为45+-10+5Xs。
* 在本篇文章中他们的模型中Zone A有4个ID检查点 Zone B有4条检查线。
* 我们不考虑不同站点之间转移的时间。
 ### The Basic Model(Liu)
* the process of waiting for screening is the most time consuming 
* Basic Model总共分为四个部分 Inflow Model 、 Attributes Generation Model 、 Queuing Model 、 Screening Model
* Inflow Model
inflow model 模拟了乘客随机到达机场入口的时间，服从泊松分布
* Attributes Generation Model 包含四个部分：ID Check 、millimeter wave scanning、Pre-r、Pre-p
* Queue Model
* Screening Model
### Modifications to the Current Process(Hu)
* 总时间分布、不同步骤时间分布、预检旅客与普通旅客比例的影响、预检通道数量与普通通道数量的比例影响
* MPL模型：多名乘客提前准备行李
* PBQ模型：基于优先级
* SP模型：特殊人群（老人、儿童）

### Model Evaluation & Sensitivity Analysis(Hu)
* 插队分析

### Conclusion(Liu)



---


## Breezing Through Security Checkpoints: an Intelligent Airport with Smart Scheduling(Team #55295)上海交大（1）

### Summary(Gao)

 1. 对任务一，对案件流程进行建模。识别出了三处瓶颈位置：缺少ID-Check口，检查口的专用性，有怀疑乘客的出现。
 2. 对任务二，建立了三个算法：greedy algorithm, backpressure algorithm, drift-plus-penalty algorithm.
 3. 对任务三，分析了不同文化（个人主义和集体主义）和不同乘客类型（家庭型，技术型）。并对不同情形提供了accomodations。
 4. 对任务四，提供了全球适用和局部适用的政策。

### Introduction(Gao)

贡献有三：

 1. 用排队模型对案件流程进行建模；用真实世界的参数组合和数据验证模型；找出三个瓶颈位置。
 2. 提出三个算法来改进模型。发现backpressure最好。
 3. 敏感性分析和相对应的措施。

### Basic Analysis of the problem(Gao)

 1. M/G/c Queue：M（乘客到达时间服从泊松分布）；G（服务时间服从任意概率分布）；c（c个检查口）
 2. 参数设置：用Mathematica中的EstimatedDistribution确定
 3. 用速率稳定性确定regfular和pre-check比例为3:1
 4. 表现测试方法：用吞吐量和方差（regular和pre-check的加权平均）

### Models(Liu)

### Simulations and Bottleneck Detection(Hu)
* 可疑乘客
* 真实乘客数据
* 缺少足够的预检查点、来自同一ID检查点的扫描检查过长、可疑乘客

### Modifications to the Process(Hu)
* 1.贪心路由算法
* 2.Lyapunov、Backpresure
* 3.Drift-Plus-Penalty算法

### Sensitivity Analysis(Hu)
* 1.集体主义文化
* 2.个人主义文化
* 3.家庭旅行者
* 4.科技旅行者

### Conclusion(Liu)

---


## Reducing Wait Times at Airport Security(Team #56632)Brown University

### Summary(Gao)

 1. 第一段：解释背景，我们的解决方案分为四部分：a queue model，a method of simulation，基于成本效益分析的应用，考虑不同乘客的修正。
 2. 第二段：我们识别出导致无效率的原因是排队过程（核密度估计（kernel density estimation）是在概率论中用来估计未知的密度函数，属于非参数检验方法之一）。
 3. 第三段：开发了一个算法来模拟过程。
 4. 第四段：用成本效益分析确定什么时候配备人员和检查乘客。
 5. 第五段：最后我们考虑乘客不同。
 6. 第六段：升华总结，世界和平。

### Introduction(Gao)

 1. 总览：
     1. Formulate a queuing model.
     2. Implement a simulation method.
     3. Analyze simulation results through cost-benefit anaylsis.
     4. Make modifications to the model.
 2. 假设
     1. 忽略站台和队伍之间的转移时间。
     2. FIFO原则
     3. 所有的工作人员同一性
     4. 乘客等待时间能够反映吞吐量

### Main Assumption
* 车站和排队之间的过境时间可以忽略不计。
* 队列按照“先进先出”(FIFO)的原则运作。
* 所有员工在工作能力方面都是一样的。 
* 所有员工都是乘客等待时间，是对吞吐量的精确测量。就他们的工作能力而言。

### A Queuing Model(Liu)

### Simulation(Hu)
* 乘客数量50-4050时，花费的时间

### Evaluation/Results(Hu)
* 1.身份检查、扫描检查
* 2.成本分析
* 3.灵敏性分析：有经验和没有经验的旅行者（快 慢）

### Improving the Model(Liu)

### Conclusion(Liu)

---


## Time Counts! Less Waiting & Better Airports(Team #67316)浙大

### Summary(Gao)

 - 开场白
 - 两阶段模型：M/M/c in Kendall notation ; M/Ek/c（Erlang）
 - 我们发现参数和文化相关
 - 还探索了修改方法必须更人性化的位置安排
 - 提出了虚拟队伍的概念，并且将FIFO变成了部分队列优先原则
 - 考虑了文化因素，添加了一个修正项
 - 总结

### Introduction(Gao)

 - 背景
     - 识别瓶颈
     - 作出修正
     - 考虑文化
     - 提出建议
 - 总览
     - 问题一，两步：Document check(Poisson queue);Luggage and body scanning(Erlangian model)
     - 问题二，考虑一个有影响力的因素进去。
     - 修正了到达时间来影响乘客的到达行为。
     - 还考虑了justifiability（合理性）

### Assumptions(Liu)
* 对于服务器、检查点结构，不考虑单个可变性。
* 尽管扫描检查过程中打开的通道数是动态的，但我们假设服务能力始终处于其最大值。也就是说，只要到达的时间超过了目前的能力，备用通道就会开放。
* 假设每个乘客都会选择在队列中等待，从而使他们在每个检查点的等待时间最小化。
* 乘客到达机场的某一特定ﬂ的时间点服从正态分布。
* 与正常情况相比，TSA Pre-check 对阻塞的影响不大。
* 几乎每个人都会提前至少一个半小时到达机场。

### Queueing Model for Security Check Process(Liu)

### Queueing Simulation for Bottlenecks Spotting(Hu)
* 1.费用评估
* 2.仿真结果 瓶颈是扫描通道数量、等待时间（脱衣服等）

### Comments on the Safety(Hu)
* 不减少检查环节，优化排队流程、人力资源安排

### Passenger Arrival Behavior Modeling(Hu)
* 客流产生：正态分布
* 不同达到时间下的仿真结果（到达时间越早，等待时间越少）

### Checkpoint Redesign(Hu)
* 实时监测每个检查点的人数，帮助乘客选择
* 人力资源分配（通道数量）
* 基于时间，动态规划检查点数量
* 敏感性分析：客流量（扫描时间）影响大，证件检查影响小

### Virtual Queueing(Hu)
* 虚拟排队（移动排队）

### Inter-cultural Applicability(Liu)

### Discussion and Conclusion(Liu)

---


## Optimizing Passenger Throughput at an Airport Security Checkpoint(Team #68942)NC School

### Summary(Gao)

- 朴素的开头
- 开发了一个利用NeyLogo的agent-base model
- 尝试了不同的布局和流量，发现了三个瓶颈位置：预检查，普通文件检查的最开始，还有普通乘客的全身检查
- 用NetLogo model看不同修正的影响
- 朴素的结尾

### Assumption(Liu)
* 每位乘客单独旅行。
* 给定的数据集代表乘客如何通过筛选过程。
* 到达是一致随机的。
* 旅行者选择人数最少的甄别通道。
* 任何美国安全检查点的总体布局与图4所示相同。
* 每两条扫描线，就有一个金属探测器和一个毫米波身体扫描仪。
* 排队没有限制。
* 每秒钟最多有一名乘客到达检查站。
* 从检查点入口步行到文档检查队列不需要时间。 
* 平均美国乘客的私人空间是3英寸乘3英寸。
* 所有乘客最终都完成了检查过程。
* 所有参加PreCheck项目的旅客都要通过wtmds。
* 每位乘客至少带一件行李。
### Definitions and Testign Parameters(Liu)

### NetLogo Model(Liu)

### Results(Hu)

* 1221配置和2243配置在0.09、0.18,、0.36、0.54、0.72乘客生成概率下的各种结果

### Improvements to the Current Process(Hu)

* 1.更多金属探测器
* 2.金属探测仪WTMD使用量
* 3.更多的毫米波扫描仪
* 4.减少搜身检查次数（时间）
* 5.增加预检旅客比例
* 6.增加预检比例和document-checkers

### Variation in Traveler Behavior(Hu)
* 1.插队
* 2.厌恶全身扫描，选择搜身检查
* 3.走得慢的人

### Policy and Procedural Recommendations(Hu)
* 1.预检查通道增加金属探测器
* 2.非预检通道增加毫米波扫描器
* 3.等等等等

### Strengths and Weakness(Liu)


