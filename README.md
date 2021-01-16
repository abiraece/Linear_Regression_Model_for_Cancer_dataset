Cancer Death_Rate Prediction

Table of Content:
1. Introduction and Data Description
2. Data Preprocessing
3. Modeling Phase
4. Evalution Metrics
5. Conclusion

Introduction and Data Description:
These data were aggregated from a number of sources including the American Community Survey (census.gov), clinicaltrials.gov, and cancer.gov.

avgAnnCount -- Mean number of reported cases of cancer diagonised annually

avgDeathsPerYear -- Mean number of reported mortalities due to cancer

TARGET_deathRate -- Mean per capita cancer mortalities

incidenceRate -- Mean per capita cancer diagoses

medIncome -- Median income per country

popEst2015 -- Population of country

povertyPercent -- Percent of populace in poverty

studyPerCap -- per capita number of cancer related clinical trials per country

binnedInc -- Median income per capita binned per decile

MedianAge -- Median Age of country Resident

MedianAgeMale -- Median Age of Male country resident

MedianAgeFemale -- Median Age of Female country resident

Geography -- Country name

AvgHouseholdSize -- Mean household size of country

PercentMarried -- Percent of country resident who are married

PctNoHS18_24 -- Percent of country resident age 18 - 24 highest education attained: less than high school

PctHS18_24 -- Percent of country resident age 18 - 24 highest education attained: high school diploma

PctSomeCol18_24 -- Percent of country resident age 18 - 24 highest education attained: some college

PctBachDeg18_24 -- Percent of country resident age 18 - 24 highest education attained: Bachelor's Degree

PctHS25_Over -- Percent of country resident age over 25 highest education attained: high school diploma

PctBachDeg25_Over -- Percent of country resident age 18 - 24 highest education attained: Bachelor's Degree

PctEmployed16_Over -- Percent of country resident age 16 and over employed

PctUnemployed16_Over -- Percent of country resident age 16 and over unemployed

PctPrivateCoverage -- Percent of country resident with private health coverage

PctPrivateCoverageAlone -- Percent of country resident with private health coverage alone(no public assistant)

PctEmpPrivCoverage -- Percent of country resident with employee provided private health coverage

PctPublicCoverage -- Percent of country resident with government provided health coverage

PctPublicCoverageAlone -- Percent of country resident with government provided health coverage alone

PctWhite -- Percent of country resident who identified as white

PctBlack -- Percent of country resident who identified as Black

PctAsian -- Percent of country resident who identified as Asian

PctOtherRace -- Percent of country resident who identified not as white, Black or Asian

PctMarriedHouseholds -- Percent of married household

BirthRate -- Number of live birth realtive to number of women in the country

Objective : To Build a multivariate Ordinary Least Squares regression model to predict "TARGET_deathRate".

Data Preprocessing:

    1. Finded datatypes of entire dataset
    2. Imputed Null Values and dropped the feature with more that 75% of missing value and other null values are imputed based on KNNImputer
    3. Encoded all categorical feature and converted into numerical feature to build model
    4. To avoid outlier to affect model performance, outlier are treated by capping method.
    
Modeling Phase:

    1. Basic Least Square model is built.
    2. To check for 5 assumption to build Linear Regression model further. 
        a. Multicollinearity effect is statisfied for some input features
        b. Normality test is statisfied with skewness of 0.1         
        c. Linearity test is statisfied 
        d. Autocorrelation test is statisfied         
        e. Homoscadacity test is also statisfied
    3. Different Feature selection algorithm are performed
    
Conclusion:
    From the above build model we can conclude that performance of the OLS model was increased using polynomial feature selection method and result was seen from 
    increased R-square.

    Overall Performance of the model was 53.7%
