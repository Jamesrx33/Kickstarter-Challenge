# **<p align="center">Theater Kickstarter Analysis</p>**

## **<p align="center">An analytics report designed to optimize the success of the _Fever_ Kickstarter campaign.</p>**

### The following will identify and display success factors of Theater Kickstarter Campaigns with a focus on _Launch Dates_ and _Funding Goals_. 

---
## Method of Analysis
1. **Analysis of Launch Date:** A Pivot Table, filtered by the "Theater" Parent Category and Year, was generated from the source data. The rows of the table were organized by Month and a count of all successful, failed and canceled campaigns were displayed for each row. From this table we generated the "Theater Outcomes Based on Launch Date" line chart to display the trend of Theater Kickstarter Outcomes throughout the months of the calendar year.

    * [Launch Date Reference Table](https://github.com/Jamesrx33/Kickstarter-Challenge/blob/main/Resources/Table_Outcomes_vs_Launch.png)

2. **Analysis of Funding Goals:** A new Sheet was created and a "Goals" table was organized using 11 disitinct Goal ranges. The number of successful, failed and canceled Theater Kickstarter Campaigns was populated using the Excel COUNTIFS() fuction. This function referenced the data in the original sheet, filtered for the "Plays" subcategory and specified the range in its respective Goals Table row. After obtaining these metrics, the Total count of projects in each range was calculated using the Excel SUM() function. Finally, the percentage of successful, failed and canceled campaigns in each range was identified by taking the dividend of each respective count over the total. The "Outcomes Based on Goal" line chart below was then generated using these percentages and their attributed range.

    * [Goals Reference Table](https://github.com/Jamesrx33/Kickstarter-Challenge/blob/main/Resources/Table_Outcomes_vs_Goals.png)

---
### Visualization of Launch Date Analysis
![Theater_Outcomes_vs_Launch](https://github.com/Jamesrx33/Kickstarter-Challenge/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Visualization of Goals Analysis
![Outcomes_vs_Goals](https://github.com/Jamesrx33/Kickstarter-Challenge/blob/main/Resources/Outcomes_vs_Goals.png?raw=true)

### Challenges and Difficulties Encountered
        >The original "launched_at" data was in written in a Unix Timestamp.
        
          - This was overcome by applying the following date conversion formula: =(((I2/60)/60)/24)+DATE(1970,1,1)
 
        >The resulting "Date Created Conversion" obtained from the Unix Timestanp needed to have the Year extracted in order to provide an applicable filter to our visualization
        
          - The Excel "Year()" formula was used to extract the Year from the converted Launch Date

        >The original data was from multiple Parent Categories that were less applicable to Louise's inquiry
        
          - The "Parent Category" data was used as a filter in our Pivot Table so we could focus solely on Theater Kickstarters
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  1. Theater Kickstarter campaigns in the month of May have the highest ratio of success.
  2. The number of failed campaigns throughout the year remains roughly constant.

- What can you conclude about the Outcomes based on Goals?

  * There is an inverse relationship between a Theater Kickstarter Campaign's Goal and Ratio of Success. As the Goal increases, the chances of success decrease.

- What are some limitations of this dataset?
  
  1. There are a variety of outliers (Campaigns with goals >$1,000,000) that skew the dataset to the right.
  2. The sample set is from multiple countries and spans 10 different Kickstarter categories.
  3. The dates of the sample Campaigns are all 4+ years old, potentially rendering them less applicable to today's market.
  4. Locations within the Countries are not specified and could prove relevant (State, City, Venue, etc).
  
- What are some other possible tables and/or graphs that we could create?

  1. A Bell Curve to validate the integrity of the data per our NULL Hypothesis(s) (I.E. "The greater the goal, the less successful campaigns")
  2. A Scatter Plot that shows the correlation between Year of the Campaign and percentage of success in each category (Theater Campaigns are X-amount more/less successful than other categories)
  3. A Table that displays the number of backers and pledged amount for each Theater campaign (An analysis of Campaigns with a high volume of backers vs high average pledged amount could prove useful)

---
## Reference Documentation - [Source Code Repository](https://github.com/Jamesrx33/Kickstarter-Challenge/tree/main)
