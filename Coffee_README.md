## Project Status: In progress 
![Imgur](https://imgur.com/kN2ygv1.gif)

# Table of Contents
- [Info](#info)
- (Data Sources)[#datasets-sourced-from:]
- (Technology Stack)[#Tech-Stack]
- (Improvement Opportunities)[#Oppurtunities-for-improvement-/-Notes]
- (The Process)[#The-Process] 

## Info
A simple analysis of my true love, coffee. Employing my skills in exploratory data analysis with various tools like ggplot2 and tidyr. 

### Questions to ask:
What are the historical trends in retail prices of various types of coffee in the US market? 

How do changes in import volumes or costs influence consumer prices? 

Are there any seasonal or cyclical patterns in coffee prices? 

## Datasets Sourced from:
* US Food Imports [https://www.ers.usda.gov/data-products/u-s-food-imports/] (Metrics given in kilos) 
* Global price of coffee from 1990 to 2024 ARABICA [https://fred.stlouisfed.org/series/PCOFFOTMUSDM]
* Global price of coffee from 1990 to 2024 ROBUSTAS [https://fred.stlouisfed.org/series/PCOFFROBUSDM]
* Consumer Price Index for All Urban Consumers: Coffee in U.S. City Average [https://fred.stlouisfed.org/series/CUSR0000SEFP01]


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

## The Process
Compiled a few sources for data and began thinnking of what i could ask of the data sets obtained
as well as how can I bring these together into one file? 
saved individual sheets from data XLS files as CSV files
installed and loaded "readr" package into R studio
changed necessary files to CSV format 
began upload and read the CSV files in R studio using the Readr package
Now I started thinking about some questions I should ask of this data...  
 
Noticed some things about the data set :
- the Import dataset is seperated into three categories within a sheet
  
1/ Sum of unroasted beans, roasted and instant coffee. Includes coffee husks and skins. 

2/ Includes coffee husks and skins and coffee substitutes. 

3/ Includes chicory and other substitutes for coffee. 

- Countries not listed in each section are assumed to not contribute to the imports in that category  
- the data I see the column after the SOURCE column might be irrelevant, I remove this column  
 
Realizing the table having these categories in one sheet causes issues for creating queries. Exported CSV , Working on separating the data into separate files in excel, then reuploading to work on them in POSIT 



  
