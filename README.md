# covidAnalysisIndia

To estimate the effect of the lockdown in India which was announced on 14/04/2020 using Robust Synthetic Control Method. 

## Donor Pool csv file

It contains the number of confirmed cases from 22/01/2020 till 18/07/2020 for India and the donor pool.

## Robust Synthetic Control 

Robust Synthetic Control (RSC) (Amjad, Shah, and Shen
2018) is a recent variation of SC that can better handle noise
and missing data. It takes a set of candidates for control
group (countries, called donor pool) and creates a synthetic
state (control group) by taking a weighted average of a con
vex combination of other countries (donor pool). RSC de
noises the data via singular value thresholding, which im
putes missing information in the data matrix. Unlike clas
sical synthetic control methods, it uses unobserved mean
values instead of noisy data. RSC is also much more ro
bust, since it overcomes the challenge of missing data and
works well in situations where sufficient covariate informa
tion may not be available. 

## Resources Used 

1. Covid Data (https://raw.githubusercontent.com/RamiKrispin/coronavirus/master/csv/coronavirus.csv)
2. Global Health Index Data (https://raw.githubusercontent.com/OxCGRT/covid-policy-tracker/master/data/OxCGRT_latest.csv)
3. Poverty Stats (https://datacatalog.worldbank.org/dataset/poverty-and-equity-database)
4. Global Mobility Report (https://www.google.com/covid19/mobility/)
5. Population Data (https://www.kaggle.com/tanuprabhu/population-by-country-2020)
6. Oxford Covid policy tracker (https://raw.githubusercontent.com/OxCGRT/covid-policy-tracker/master/data/OxCGRT_latest.csv)

## Methodology

I filtered our donor pool based on various predictor variables such as income levels, population, movement restrictions and global mobility to find countries that were comparable to India during the pre intervention period.
After that we performed our RSC using tslib library implementation and using no. of confirmed Covid cases as outcome variables.


