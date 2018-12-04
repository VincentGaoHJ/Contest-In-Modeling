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
* **Put forward two kinds of model**
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

### Data Processing

#### Data Screening(Liu)

#### Data imputation(Liu)

#### Data Normaliztion(Liu)

### ROI Evaluation

#### Concept of ROI(Liu)

#### Using Grey Theory to Predict ROI(Liu)

### Model Construction

#### Definition of Risk(Liu)

#### Basic Model(Liu)

#### Results of Basic Model(Hu)

#### Time Series Model(Liu)

#### Results of Time Series Model(Hu)

### Sensitive analysis and validation

#### Risk-Return(Hu)

#### School Number(Hu)

#### Policy of Distribution(Hu)

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

#### weaknesses(Hu)

### News Release(Gao)



---

## The Optimal Investment Strategy Based on the Large--scale Non-linear Constraint Optimization Methods (Team #47823)

### Summary(Gao)

### Problem Statement(Gao)

### Assumptions(Liu)

### Data Analysis and Focus Decision(Liu)

### School Selecting(Liu)

### Strategy Making(Liu)

### Result(Hu)

### Test our model(Hu)

### Conclusion(Hu)

### Letters to the CFO(Gao)

---

## An Optimal Strategy of Donation for Educational Purpose (Team #42939)

### Summary(Gao)

### Introduction(Gao)

### Addressing the Missing Values(Liu)

### Determining the Performance Index(Liu)

### Identifying Performance Contributing Variables via Post-LASSO(Liu)

### Determining Investment Strategy based on ROI(Liu)

### Extended Model(Hu)

### Conclusions and Discussion(Hu)

### Letters to the CFO(Gao)

---

## A Multilevel Bayesian Model based on Economic Contribution of University Alumni (Team #52815)

### Summary(Gao)

### Introduction(Gao)

### Data Cleaning and Imputation Schema(Liu)

### Model Components(Liu)

### Solving the Optimization Problem(Hu)

### Problem Statement and Special Considerations(Liu)

### Model Analysis(Hu)

### Results from Model(Hu)

### Conclusion(Hu)

### Letters to the CFO(Gao)
