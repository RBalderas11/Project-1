Project-1 - Impact of Insurance and Income on Heart Disease Mortality
Team Members: Abdulla Mashaly, Elijah Reid, Hannah Doby, and Rebecca Balderas

Project Description:
For this project, we researched the impact of insurance and income on heart disease mortality. We conducted the research through the use of data compiled through the Census Bureau and Centers for Disease Control. 
We focused our research on the state of North Carolina. We pulled income level in relation to the poverty line by county from the census bureau. We also pulled data from a study conducted by the US goverment regarding
heart mortality by county. 

Research Questions to Answer:

1. If an individual has insurance, are they less likely to die from heart disease? 2 geographical maps, 1 scatterplot
       
2. Is an individual in a higher income bracket more likely to be insured? ttest, box and whisker
        
3. Does the total population in a given county coorelate with the amount of individuals insured? 2 bar graphs, 1 pie chart

Alternative hypothesis: The lower income population is less likely to be insured
/n
Null hypothesis: Income levels have no affect on percentage covered
    We ran a T-test on the insurance coverage data by income, comparing the highest income bracket (Over 400% of Poverty) and the lowest income bracket (Under 138% of Poverty) and received a p-value of less than 0.05, so the null hypothesis can be rejected, and lean further into the credibility of the alternative hypothesis being true.

Data Sets to be Used:

United States Census Bureau - Small Area Health Insurance Estimates - https://api.census.gov/data/timeseries/healthins/sahie?get=NIC_PT,NUI_PT,AGE_DESC,AGECAT,NAME&for=county:*&in=state:37&time=2019

Centers for Disease Control - https://data.cdc.gov/Heart-Disease-Stroke-Prevention/Rates-and-Trends-in-Heart-Disease-and-Stroke-Morta/7b9s-s8ck

Data Needs:
There are some additional programs that will be needed for the graphs and maps to show:
Geopandas
Hvplot

## Data Sources
### Small Area Health Insurance Estimates (SAHIE) Program
The Small Area Health Insurance Estimates (SAHIE) program was created to develop model-based estimates of health insurance coverage for counties and states. This program builds on the work of the Small Area Income and Poverty Estimates (SAIPE) program. SAHIE is the only source of single-year health insurance coverage estimates.
SAHIE data can be used to analyze geographic variation in health insurance coverage, as well as disparities in coverage by race/ethnicity, sex, age and income levels that reflect thresholds for state and federal assistance programs. Because consistent estimates are available from 2008 to 2020, SAHIE reflects annual changes over time.
- Data Source <https://www.census.gov/programs-surveys/sahie/about.html>
- Terms os Service <https://www.census.gov/data/developers/about/terms-of-service.html>
### Rates and Trends in Heart Disease and Stroke Mortality Among US Adults (35+) by County, Age Group, Race/Ethnicity, and Sex – 2000-2019
This dataset documents rates and trends in heart disease and stroke mortality. Specifically, this report presents county (or county equivalent) estimates of heart disease and stroke death rates in 2000-2019 and trends during two intervals (2000-2010, 2010-2019) by age group (ages 35–64 years, ages 65 years and older), race/ethnicity (non-Hispanic American Indian/Alaska Native, non-Hispanic Asian/Pacific Islander, non-Hispanic Black, Hispanic, non-Hispanic White), and sex (women, men). The rates and trends were estimated using a Bayesian spatiotemporal model and a smoothed over space, time, and demographic group. Rates are age-standardized in 10-year age groups using the 2010 US population.
- Data source: National Vital Statistics System <https://data.cdc.gov/Heart-Disease-Stroke-Prevention/Rates-and-Trends-in-Heart-Disease-and-Stroke-Morta/7b9s-s8ck>
## Data Limitations
1. **Sample Size and Coverage:** The data used in this analysis is based on specific sources, such as the Census Bureau and the Centers for Disease Control (CDC), which may have limitations in terms of sample size and geographical coverage. Consequently, some counties or regions may have limited or missing data, which could impact the generalizability of the findings.
2. **Data Quality and Completeness:** Data quality vary across our two sources of data. In the SAHIE data, ages of 65 and over are not included, as most people ages 65 and over are covered by Medicare or Supplemental Security Income (SSI). According to recent CPS ASEC data, less than 2 percent of the 65+ population were uninsured nationwide. In the Mortality data, ages below 35 are not included in the dataset. We have taken steps to clean and preprocess the data, but some inaccuracies may still persist.
3. **Temporal Scopes:** The data used in this project only covers year 2019. It's important to note that trends and patterns may have changed over time.
4. **Causation vs. Correlation:** While our analysis explores relationships between income, insurance coverage, and heart disease mortality, it is essential to understand that correlation does not imply causation. Other factors may influence those relationships.

1.  According to our graphs and data, it can be concluded that yes, if an individual has insurance, they are less likely to die from heart disease. Referring to the two geographical maps of the NC counties that show the mortality numbers by county and percent insured by county respectively, it is clear that the "darker colored" counties on the mortality map, are shown on the percent insured map as "lighter colors". 