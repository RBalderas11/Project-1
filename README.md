# Project-1: Impact of Insurance and Income on Heart Disease Mortality

## Team Members

- Abdulla Mashaly
- Elijah Reid
- Hannah Doby
- Rebecca Balderas

## Project Description

In this project, we researched the impact of insurance coverage on heart disease mortality in year 2019, in the state of North Carolina. Our research was based on data compiled from the Census Bureau and the Centers for Disease Control (CDC). We focused on understanding the relationship between health insurance coverage and income levels in relation to the poverty line and the relationship between health insurance coverage and heart disease mortality rates at the county level.

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

2. **Data Quality and Completeness:** Data quality vary across our two sources of data. In the SAHIE data, ages of 65 and over are not included, as most people ages 65 and over are covered by Medicare or Supplemental Security Income (SSI). According to recent CPS ASEC data, less than 2 percent of the 65+ population were uninsured nationwide. In the Mortality data, ages below 35 are not icluded in the dataset. We have taken steps to clean and preprocess the data, but some inaccuracies may still persist.

3. **Temporal Scopes:** The data used in this project only covers year 2019. It's important to note that trends and patterns may have changed over time.

4. **Causation vs. Correlation:** While our analysis explores relationships between income, insurance coverage, and heart disease mortality, it is essential to understand that correlation does not imply causation. Other factors may influence those relationships.

## Research Questions

- If an individual has insurance, are they less likely to die from heart disease?

- Is an individual in a higher income bracket more likely to be insured?

- Does the total population in a given county coorelate with the amount of individuals insured?

## Data Retieval and Cleaning

The data is obtained through an API request to the Census Bureau's API, specifically the Small Area Health Insurance Estimates (SAHIE) dataset. The API request fetches insurance-related data for the year 2019 for all counties in North Carolina. The retrieved data is converted into a Pandas DataFrame, where the columns are appropriately renamed for clarity. Unused columns and rows are dropped, and the DataFrame is further cleaned and organized.

The insured and uninsured populations are calculated for different age categories and income categories within each county. The data is then aggregated into two new DataFrame, clean_insurance_by_age and clean_insurance by_income containing information on the number of insured and uninsured individuals for various age and income categories in each county. Then, The percentages of insured and uninsured populations are calculated based on the aggregated data.

## Data Analysis and Visualization

### Used Modules:
- Pandas
- Numpy
- Matplotlib
- Requests
- JSON
- Scipy
- Geopandas
- Hvplot

---
1. In our first research question, we examine the correlation between health insurance coverage and mortality rates of heart disease through the following:

### Percentage of Insured Population per County

In this section, we present the data visualization of the percentage of insured population in each county of North Carolina. The visualization showcases the geographic distribution of insurance coverage across the counties, providing valuable insights into the variation of insured population percentages. The interactive heatmap plot uses a color gradient (cmap="YlOrRd") to represent the range of insurance coverage percentages. Counties are colored according to their respective percentage of insured population, and hovering over a county displays additional information, including the county name and the corresponding percentage of insured population. This data visualization offers an intuitive and geospatial perspective of insurance coverage, helping us identify regions with varying levels of insured population percentages.

![Percentage of Population Insured Per County][assets/images/Perncetage_insured.png]

### Mortality Rates per County
### Correlation analysis

---
2. The second question was trying to determine if there is a correlation between the income categories and the health insurance coverage

### Outliers Analysis and Boxplot Visualization
An outlier analysis was performed on the percentage of insured population data based on income categories. The goal is to identify potential outliers in the dataset using the Interquartile Range (IQR) method. This outlier analysis provides a quantitative assessment of data points that deviate significantly from the typical range, allowing for further investigation and consideration of their impact on the analysis results. 

Outliers per income category were: 
- Over 400% of Poverty's: 88.239816, 89.349112, 87.489556, 84.823529
- 250% to 400% of Poverty's: 82.793585, 80.189093, 82.531146, 78.733572
- 200% to 250% of Poverty's: 75.079940, 87.778861, 76.111003, 75.170843

Thes information was visualized through a box plot, The box plot allow for a clear comparison of the spread and central tendencies of the insurance coverage percentages for each income category. We can make an observation that there appears to be a trend of higher insurance coverage percentages for higher income categories. However, we run a T-Test to make a statistical comparison between income and health insurance coverage.

![Box Plot](assets/images/box_plot.png)

### T-Test for Health Insurance Coverage and Income
This test compares the percentage of insured population between two income categories: "Over 400% of Poverty" and "Under 138% of Poverty.", and allows for a statistical comparison of the means of the percentage insured between these two income groups.
Alternative hypothesis: The lower income population is less likely to be health insured.
Null hypothesis: Income levels have no affect on percentage of population with health insurance coverage.

Based on the t-test results, The **t-statistic** is approximately 38.28. This value represents the difference in means between the two groups, taking into account the variation within each group. The **p-value** is approximately 1.17e-80. This p-value is extremely small, essentially being zero. With such a small p-value, we can confidently reject the null hypothesis. The null hypothesis assumes that there is no significant difference between the percentage of insured population for high-income and low-income individuals. However, the extremely low p-value suggests strong evidence that there is a statistically significant difference in insurance coverage between these two income groups.
---
3. 













Conclusion:
Based on the t-test results, there is a significant difference in the percentage of insured population between individuals with incomes "Over 400% of Poverty" and "Under 138% of Poverty." This finding may have important implications for understanding how income levels impact insurance coverage rates in the context of heart disease mortality analysis in North Carolina.



