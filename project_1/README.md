# Project 1: Standardized Test 

## Overview

### Problem Statement
We are consultants hired by the U.S Department of Education, researching on which state(s) to assist in improving participation rates and/or scores for SAT and/or ACT in the United States so resources may be allocated appropriately. 

For this study, we will be researching if there is a score bias for households with higher or lower median income with regards to SAT/ACT participation rates and scores. 

We will look into the following:

- Are there any correlation between SAT and ACT participation rates and scores as well as external factor?
- Are there score or participation rate bias for households with higher or lower median income?



## Background

For this project, we're going to take a look at aggregate SAT and ACT scores and participation rates in the United States. We'll seek to identify trends in the data and combine our data analysis with outside research to address our problem statement.

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

## Datasets

For the purpose of this study, we will be using the following datasets which may be found in the [`data`](./data/) folder:

* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`median_family_income_2019.csv`](./data/median_family_income_2019.csv): 2019 median family income ([source](https://www.census.gov/data/tables/time-series/demo/income-poverty/historical-income-households.html))
* [`US_region_state.xlsx`](./data/US_region_state.xlsx): US states by region ([source](https://www.bea.gov/data/by-place-states-territories))


#### Additional Research

- Increase in income inequality in the United States over the recent years. ([*source*](https://www.pewresearch.org/social-trends/2020/01/09/trends-in-income-and-wealth-inequality/#:~:text=Over%20the%20same%20period%2C%20the,in%20the%20decades%20since%201980))

- How median family income affects ACT composite scores. ACT composite score by Family Income([*source*](https://www.act.org/content/dam/act/unsecured/documents/R1604-ACT-Composite-Score-by-Family-Income.pdf))

- ACT and SAT mandatory States in the United States ([*source*](https://prepmaven.com/blog/test-prep/states-require-sat-act/))



#### Data dictionary

| Data | Description |
| --- | --- |
| **act_2019** | 2019 ACT composite scores by States
| **sat_2019** | 2019 ACT composite scores by States  
| **median_family_income_2019** | 2019 median family income |
| **US_region_state** | US states by region |


### Summary of analysis

During the data analysis, the following have been noted:

- Regions may play a part in ACT/SAT scores. Notably, highest ACT scores are mostly from the Northeast region. However, participation rates from these region's states are relatively low.
- Likewise, highest SAT scores are prevalent in the Midwest region. Similarly, participation rates are relatively low for states with the highest SAT scores.
- As participation rates for SAT increases, participation rates for ACT test generally decreases. (inverse correlation)
- The higher the participation rate or either SAT or ACT test, the lower the score generally.
- There are no states with participation rates and scores for both SAT & ACT being above the average.
Only Massachusetts & Virginia have family income > avg, as well as SAT & ACT scores above average. 
- States


### Conclusion and Recommendations

Based on the studies above, the higher the participation rates for SAT & ACT tests, the lower the scores generally. We have learnt that there is also a positive correlationship between median family income and ACT composite scores. Students are also more likely to be biased towards a test rather than taking both SAT & ACT test concurrently.

Looking into the different regions, the Southeast and Southwest regions faired the worst. All the states in those regions except for Virginia fell below the national average ACT score and national average median family income. 

From the barplot of the Southern regions and ACT/SAT participation rates, only two states stood out. North and South Carolina were the only two states with participation rates above the national average participation rate for both test. As North Carolina already has a state mandate on ACT participations, it would be likely that there is already an educational infastructure for ACT test. As compared to states with mandatory SAT parcipations, efforts to increase ACT scores in these states may be marginal.

Futhermore, despite ACT test not being mandatory, the participation rate exceeds the national average. This could be an indicator that students signed up for the ACT test have expressed greater interest and hence may be keen in improving their scores. 

Therefore, the recommended state for improving ACT scores would be **South Carolina**.

**Recommendations**:

- Making practice resources more readily available (eg: e-learning, online resources, school libraries) for free or at subsidized rates.
- Increase educational funding (better teaching & learning equipment/ learning facilities/ better welfare)
- Raise standards for teachers/professors. 
- Incentivize University enrollment / acceptances for students.
- Raise awareness through campaigns.

