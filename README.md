## Project Overview
According to World Health Organization (WHO), cancer is the second leading cause of death globally and is responsible for an estimated 9.6 million deaths in 2018. Globally, about 1 in 6 deaths is due to cancer. Approximately 70% of deaths from cancer occur in low- and middle-income countries. Among the leading causes of cancer are high body mass index, low fruit and vegetable intake, lack of physical activity, tobacco use and alcohol use. However, many aspects of the behaviour of cancer disease are highly unpredictable. Even with the huge number of studies that have been done on the DNA mutation responsible for the disease, we are still unable to use this information at the clinical level. We must also understand other aspects of human life such as social and economic factors that are likely to impact the possibility of the occurrence of cancer and leverage them to predict the death rate due to the disease.

## Objective
This project aims to develop an ML regression model that predicts the cancer death rate in the USA using clinical, social and economic data. [Here](https://github.com/Popseli/Predicting_Cancer_Death_Rate) is the Github link of the dataset and codes of the project.

## Data
A dataset of 3,048 records were collected from clinicaltrials.gov, cancer.gov and the US Census American Community Survey. The data consists of 34 variables including the target variable as described below:
- TARGET_deathRate: Dependent variable. Mean per capita (100,000) cancer mortalities(a)
- avgAnnCount: Mean number of reported cases of cancer diagnosed annually(a)
- avgDeathsPerYear: Mean number of reported mortalities due to cancer(a)
- incidenceRate: Mean per capita (100,000) cancer diagoses(a)
- medianIncome: Median income per county (b)
- popEst2015: Population of county (b)
- povertyPercent: Percent of populace in poverty (b)
- studyPerCap: Per capita number of cancer-related clinical trials per county (a)
- binnedInc: Median income per capita binned by decile (b)
- MedianAge: Median age of county residents (b)
- MedianAgeMale: Median age of male county residents (b)
- MedianAgeFemale: Median age of female county residents (b)
- Geography: County name (b)
- AvgHouseholdSize: Mean household size of county (b)
- PercentMarried: Percent of county residents who are married (b)
- PctNoHS18_24: Percent of county residents ages 18-24 highest education attained: less than high school (b)
- PctHS18_24: Percent of county residents ages 18-24 highest education attained: high school diploma (b)
- PctSomeCol18_24: Percent of county residents ages 18-24 highest education attained: some college (b)
- PctBachDeg18_24: Percent of county residents ages 18-24 highest education attained: bachelor's degree (b)
- PctHS25_Over: Percent of county residents ages 25 and over highest education attained: high school diploma (b)
- PctBachDeg25_Over: Percent of county residents ages 25 and over highest education attained: bachelor's degree (b)
- PctEmployed16_Over: Percent of county residents ages 16 and over employed (b)
- PctUnemployed16_Over: Percent of county residents ages 16 and over unemployed (b)
- PctPrivateCoverage: Percent of county residents with private health coverage (b)
- PctPrivateCoverageAlone: Percent of county residents with private health coverage alone (no public assistance) (b)
- PctEmpPrivCoverage: Percent of county residents with employee-provided private health coverage (b)
- PctPublicCoverage: Percent of county residents with government-provided health coverage (b)
- PctPubliceCoverageAlone: Percent of county residents with government-provided health coverage alone (b)
- PctWhite: Percent of county residents who identify as White (b)
- PctBlack: Percent of county residents who identify as Black (b)
- PctAsian: Percent of county residents who identify as Asian (b)
- PctOtherRace: Percent of county residents who identify in a category which is not White, Black, or Asian (b)
- PctMarriedHouseholds: Percent of married households (b)
- BirthRate: Number of live births relative to number of women in county (b)
         (a): years 2010-2016
         (b): 2013 Census Estimates
     
## Task Performed
To accomplish the objective of the project, the following tasks were performed:
- Data profiling
- Data cleaning
- Exploration data analysis
- Feature correlation analysis
- Feature encoding
- Feature selection
- Model evaluation
- Hyperparameter tuning
- Visualization of the model's performance
- Model explainability and feature importance analysis

## Key Software and Libraries Used
* Python
* Scikit-learn
* Numpy
* Pandas
* Matplotlib
* Seaborn
* SHAP

## Prediction Results Summary

![](/images/Model%20Results%205.png)

CatBoostRegressor was observed to outperform the other algorithms by achieving the highest R squared score of 0.55, and the least MAE and RMSE of 13.84 and 18.66 respectively. After tuning the algorithm, the optimal R squared of 0.56, MAE of 13.41 and RMSE of 17.56 were achieved. The images below show demostrate the model's performance, indicating highly accurate estimation of the death rate.

![](/images/Visualizing%20model's%20performance.png)

## Model Explainability and Feature Importance Analysis
The model's explainability analysis using SHAP (shown below) indicates the ranking of the features in terms of their prediction importance whereby 'incidenceRate' is observed to be the most useful feature for the prediction task whereas 'PercentMarried' is the least useful one.

![](/images/Model%20explainability.png)
