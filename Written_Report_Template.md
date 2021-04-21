# Kickstarting with Excel

## A data analytics report designed to optimize Louise's Kickstarter campaign for the play _Fever_.

### The following will identify and display success factors in regards to previous US Plays Kickstarter campaigns with a focus on Launch Dates and Funding Goals. 
---
## Method of Analysis
1. **Analysis of Launch Date:** A Pivot Table, filtered by the "Theater" Parent Category and Year, was generated from the source data. The rows of the table were organized by Month and a count of all successful, failed and canceled campaigns were displayed for each row. From this table we generated the "Theater Outcomes Based on Launch Date" line chart to display the trend of Theater Kickstarter Outcomes throughout the months of the calendar year.

2. **Analysis of Funding Goals:** A new Sheet was created and a "Goals" table was organized using 11 disitinct Goal ranges. The number of successful, failed and canceled Theater Kickstarter Campaigns was populated using the Excel COUNTIFS() fuction. This function referenced the data in the original sheet, filtered for the "Plays" subcategory and specified the range in its respective Goals Table row. After obtaining these metrics, the Total count of projects in each range was calculated using the Excel SUM() function. Finally, the percentage of successful, failed and canceled campaigns in each range was identified by taking the dividend of each respective count over the total. The "Outcomes Based on Goal" line chart below was then generated using these percentages and their attributed range.
---
### Visualization of Launch Date Analysis
![Theater_Outcomes_vs_Launch](https://github.com/Jamesrx33/Kickstarter-Challenge/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Visualization of Goals Analysis
![Outcomes_vs_Goals](https://github.com/Jamesrx33/Kickstarter-Challenge/blob/main/Resources/Outcomes_vs_Goals.png?raw=true)

### Challenges and Difficulties Encountered
        >The original "launched_at" data was in written in a Unix Timestamp.
        
          - This was overcome by applying the following date conversion formula: =(((I2/60)/60)/24)+DATE(1970,1,1)
 
        >Our resultant "Date Created Conversion" data needed to have the Year extracted in order to provide an applicable filter to our visualization
        
          - The Excel "Year()" formula was used to extract the Year from the Launch Date

        >The original data was from multiple Parent Categories that were less applicable to Louise's inquiry
        
          - The "Parent Category" data was used as a filter in our Pivot Table so we could focus solely on Theater Kickstarters
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
