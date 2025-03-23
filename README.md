# Tennessee County Classification

When analyzing county-level data, it is often valuable to assess factors such as the degree of rurality, level of economic development, or the intrastate region of a county. This repository contains an R script that creates a file that seamlessly integrates with Census data using the GEOID field provided in Census API responses. The script includes classifications of Tennessee counties based on the following criteria:

1. Appalachian Regional Commission (ARC) distressed county status for FY2017 through FY2025;
2. Membership in a Core-Based Statistical Area;
3. Tennessee Development District;
4. Rurality as determined by the Tennessee Department of Economic and Community Development;
5. USDA Rural-Urban Continuum Codes - 2013 and 2023 vintages;
6. Census Bureau Rurality as based on rural population for 2010 and 2020 Censuses;
7. Tennessee Grand Divisions;
8. Tennessee Department of Transportation (TDOT) District; and 
9. County number.

The resulting file includes the following thirty-one variables:
1. geoid - (character) Five digit county FIPS code. 
2. county_long - County name including "County" after name
3. county - County name without "County after name
4. arc_county - Indicates if county is covered by Appalachian Regional Commission (ARC)      
5. distress_fy25 - ARC County status (Distressed, At-Risk , Transitional, Competitive, Attainment) for FY25
6. distress_fy24 - ARC County status for FY24
7. distress_fy23 - ARC County status for FY23
8. distress_fy22 - ARC County status for FY22   
9. distress_fy21 - ARC County status for FY21
10. distress_fy20 - ARC County status for FY20
11. distress_fy19 - ARC County status for FY19
12. distress_fy18 - ARC County status for FY18   
13. distress_fy17 - ARC County status for FY217
14. cbsa_code - code identifier for county in Core-Based Statistical Area (CBSA)
15. cbsa_title - name of the CBSA
16. metro_micro - indicator of whether the CBSA is a Micropoitan or Metropolitan statistical area    
17. central_outlying - indicator of whether the county is central or outlying in the statistical area
18. dev_dist_name - Name of Tennnessee Development District
19, dev_dist_acronym - Acronym for Tennnessee Development District
20. ecd_rural - Tennessee Department of Economic and Community Development county rurality designation      
21. rucc_2013 - US Department of Agriculture (USDA) Rural-Urban Continuum Codes (RUCC) for 2013        
22. rucc_2013_desc - Metadata for 2013 USDA RUCC
23. rucc_2023 - USDA RUCC for 2023
24. rucc_2023_desc - Metadata for 2023 USDA RUCC  
25. pct_rural_2010 - Percentage of county popuation that is rural, 2010 Census
26. urban_rural_2010 - Rural classification based on 2010 rural population (see detail below)
27. pct_rural_2020 - Percentage of county popuation that is rural, 2020 Census
28. urban_rural_2020 - Rural classification based on 2020 rural population (see detail below)
29. county_number - Tennessee county number assigned alphabetically
30. grand_division  - County assignment to Tennessee Grand Division 
31. tdot_region - County assignment to Tennessee Department of Transportation (TDOT) Region

### Appalachian Regional Commission (ARC) distressed county status for FY2017 through FY2025
The ARC provides data on the classification og counties being economincalily destressed. A description of the moethodology the ARC uses to classify counties can be found at: 
https://www.arc.gov/distressed-designation-and-county-economic-status-classification-system/

### Membership in a Core Based Statistical Area

2023 OMB standards for delineating CBSAs
https://www.whitehouse.gov/wp-content/uploads/2023/07/OMB-Bulletin-23-01.pdf

All 95 counties will not be in data set b/c not all counties are part of a CBSA. 

###  Tennessee Development District
Development districts are regional planning and economic organizations owned and operated by the cities and counties of Tennessee. The nine development districts were established by the general assembly under the Tennessee DevelopmentDistrict Act of 1965.
A good narrative on Development Districts
 https://tennesseeencyclopedia.net/entries/development-districts/

### Rurality as determined by the Tennessee Department of Economic and Community Development


### USDA Rural-Urban Continuum Codes - 2013 and 2023 vintages

https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/documentation
The 2023 Rural-Urban Continuum Codes distinguish U.S. metropolitan (metro) counties by the population size of their metro area, and nonmetropolitan (nonmetro) counties by their degree of urbanization and adjacency to a metro area. The division of counties as either metro or nonmetro, based on the 2023 Office of Management and Budget (OMB) delineation of metro areas, is further subdivided into three metro and six nonmetro categories. Each county and census-designated county-equivalent in the United States, including those in outlying territories, is assigned one of these nine codes. The codes allow researchers, policy makers, and others to view county-level data by finer residential groups—beyond metro and nonmetro—when analyzing trends related to population density and metro influence.
Each county and census-designated county-equivalent in the United States is assigned a code, including those in outlying territories.


### Census Bureau Rurality as based on rural population for 2010 and 2020 Censuses
 https://www.census.gov/newsroom/blogs/random-samplings/2016/12/rurality_matters.html
 "We used the 2010 definition of urban and rural as determined by the decennial
 census population. The counties were delineated as mostly urban (less than 
 50.0 percent of the county population lived in rural areas), mostly rural 
 (50.0 to 99.9 percent lived in rural areas), and completely rural (100.0 percent
 lived in rural areas)." "

 2020 Guidance
 https://www.census.gov/programs-surveys/geography/guidance/geo-areas/urban-rural.html

 2010 Guidance
 https://www.census.gov/programs-surveys/geography/guidance/geo-areas/urban-rural/2010-urban-rural.html

 Differences between  2010 Census to 2020 Census Urban Area Criteria
 https://www2.census.gov/geo/pdfs/reference/ua/Census_UA_CritDiff_2010_2020.pdf

### Tennessee Grand Divisions
 Discussion of Tennessee Grand Divisions - East, Middle & West
 https://en.wikipedia.org/wiki/Grand_Divisions_of_Tennessee
 East - https://en.wikipedia.org/wiki/East_Tennessee
 Middle - https://en.wikipedia.org/wiki/Middle_Tennessee
 West - https://en.wikipedia.org/wiki/West_Tennessee

 Tennessee Grand Divisions are codified in state law
 See Tennessee Code Annotated 4-1-201 et. seq.
 Free access to Tennessee code at:
 https://www.tncourts.gov/Tennessee%20Code

### Tennessee Department of Transportation (TDOT) District

### County number

