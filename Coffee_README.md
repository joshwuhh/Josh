## Project Status: In progress 
![Imgur](https://imgur.com/kN2ygv1.gif)

# Table of Contents
- [Purpose](#purpose)
- [Data Sources](#dataset-sources)
- [Technology Stack](#tech-stack)
- [Improvement Opportunities](#oppurtunities-for-improvement-/-notes)
- [Understanding Requirements](#understanding-requirements) 
- [Building the Data](#building-data-source)
- [Building the Charts](#building-charts)

## Purpose
The purpose of this dashboard will be to provide an overview of metrics and trends to analyze year-to-year growth of given countries exports to the US. 
A simple analysis of my true love, coffee. Employing my skills in exploratory data analysis with various tools like ggplot2 and tidyr. 

### Questions to ask:
What are the historical trends in retail prices of various types of coffee in the US market? 

How do changes in import volumes or costs influence consumer prices? 

Are there any seasonal or cyclical patterns in coffee prices? 

## Dataset Sources
* US Food Imports [https://www.ers.usda.gov/data-products/u-s-food-imports/] (Metrics given in kilos) 
<!--- * Global price of coffee from 1990 to 2024 ARABICA [https://fred.stlouisfed.org/series/PCOFFOTMUSDM]
* Global price of coffee from 1990 to 2024 ROBUSTAS [https://fred.stlouisfed.org/series/PCOFFROBUSDM]
* Consumer Price Index for All Urban Consumers: Coffee in U.S. City Average [https://fred.stlouisfed.org/series/CUSR0000SEFP01] --->


<!--- Further Develop --->
## Tech Stack

### Computing Platform
- [Posit Cloud](https://posit.co/products/cloud/cloud/)

### Packages for data pre-processing
- [Tidyr](https://tidyr.tidyverse.org/)
- [Dplyr](https://dplyr.tidyverse.org/)
- Both which are core packages within, [Tidyverse](https://www.tidyverse.org/)
### Data visualisation tool
- [Ggplot2](https://ggplot2.tidyverse.org/)


<!--- Points to add ---> 

## Oppurtunities for improvement / Notes
- Dataset for US imports needs sheets and data to be seperated and cleaned. This is being done then reuploaded into cloud IDE for analysis.
- Visualizations to be exported / redone within tableau
- adding more data from more other sources
- adding more analyses by region or country level
- extending the analysis not only to coffee, but other drink products within dataset
  
<!--- ## Acknowledgements ---> 

## Understanding Requirements
KPI Overview: Display an overview of total quantity or value of import for countries this year and previous years

Trends: Identify year and countries with highest exports to US and make them easy to recognize 

Comparison: Compare exports for each category of coffee export


## Building Data Source 
Compiled a few sources for data and began thinking of what i could ask of the data sets obtained
as well as how can I bring these together into one file? 

installed and loaded "readr" package into R studio
changed necessary files to CSV format 
began upload and read the CSV files in R studio using the Readr package
Now I started thinking about some questions I should ask of this data...  
...

Noticed some things about the data set :
- the Import dataset is seperated into three categories within a sheet
  
1/ Sum of unroasted beans, roasted and instant coffee. Includes coffee husks and skins. 

2/ Includes coffee husks and skins and coffee substitutes. 

3/ Includes chicory and other substitutes for coffee. 

- Countries not listed in each section are assumed to not contribute to the imports in that category  
- the data I see the column after the SOURCE column might be irrelevant, I remove this column  
 
Realizing the worksheet has these categories in one sheet causes issues for creating queries. Exported CSV , Working on separating the data into separate files in excel, then reuploading to work on them in POSIT 

Data in Excel is cleaned as it seems to have been prepared for end user. 
Removed descriptive cells that stated what kind of values were used.

Categories seperated into seperate sheets, then data is transposed so that the YEAR is in a column and each countries import value / weight is in rows. 

Might be useful to seperate each country into individual years but this can likely be done in notebook / Tableau 
...

Verified Date Types are the same between tables
All tables are facts. Put together the data model into Tableau Public. 

## Building Charts

Dashboard to compare year performance should be dynamic in that it should allow user to historical data that offers them flexibility to select any given year

As well it might be useful to allow user to select the category for which the chart is presenting data for. 

This can be done by creating a **List Parameter** within Tableau with **Calculated Fields**

I began this process but need to figure out why my data is not able to be shown in table format. 







  
