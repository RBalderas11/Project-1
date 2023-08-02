Project-1 - Impact of Insurance and Income on Heart Disease Mortality
Team Members: Abdulla Mashaly, Elijah Reid, Hannah Doby, and Rebecca Balderas

Project Description:
For this project, we researched the impact of insurance and income on heart disease mortality. We conducted the research through the use of data compiled through the Census Bureau and Centers for Disease Control. 
We focused our research on the state of North Carolina. We pulled income level in relation to the poverty line by county from the census bureau. We also pulled data from a study conducted by the US goverment regarding
heart mortality by county. 

Research Questions to Answer:

1. If an individual has insurance, are they less likely to die from heart disease?
        According to our graphs and data, it can be concluded that yes, if an individual has insurance, they are less likely to die from heart disease. Referring to the two geographical maps of the NC counties that show the mortality numbers by county and percent insured by county respectively, it is clear that the "darker colored" counties on the mortality map, are shown on the percent insured map as "lighter colors". 
2. If an individual is below the poverty line, are they more likely to die from heart disease?
        
3. Is there a significant impact to an individual's ability to survive heart disease due to their income and insurance coverage?

Alternative hypothesis: The lower income population is less likely to be insured
Null hypothesis: Income levels have no affect on percentage covered
    We ran a T-test on the insurance coverage data by income, comparing the highest income bracket (Over 400% of Poverty) and the lowest income bracket (Under 138% of Poverty) and received a p-value of less than 0.05, so the null hypothesis can be rejected, and lean further into the credibility of the alternative hypothesis being true.

Data Sets to be Used:

United States Census Bureau - Small Area Health Insurance Estimates - https://api.census.gov/data/timeseries/healthins/sahie?get=NIC_PT,NUI_PT,AGE_DESC,AGECAT,NAME&for=county:*&in=state:37&time=2019

Centers for Disease Control - https://data.cdc.gov/Heart-Disease-Stroke-Prevention/Rates-and-Trends-in-Heart-Disease-and-Stroke-Morta/7b9s-s8ck

Data Needs:
There are some additional programs that will be needed for the graphs and maps to show:
Geopandas
Hvplot