# Kickstarting with Excel

## Overview of Project
This project was given to us by a friend, Louise, a playwright interested in the effectiveness of kickstarter campaigns for plays. She wanted to collect information so that she could use it to inform her own campaigns for future projects. Her main concern, and the focus of this project, was the efficacy of campaigns based on their start date and target goal. With this information she hopes to create smarter, more reliable campgains, that reach the desired goal as quickly and smoothly as possible. 

## Analysis and Challenges
Louise had main two requests, an Analysis of Outcomes Based on their Launch Date, and an Analysis of the Outcomes Based on Target Goals. The challenge with both of these was to create a readable display of information that Louise could reference when planning out her own campaign. Louise provided us with ample data to complete these tasks, but one difficulty we faced with both projects was establishing what the most important pieces of information were, and how to gather them. In both cases we were able to use Excel's filtering, sorting, and formuelaic capabilities to overcome these issues and provide valuable information. The case specific information is reviewed below. 

### Analysis of Outcomes Based on Launch Date
Louise's first request was that we gather campaign data based on start date, to see if that had any effect on the success or failure of the campaign. The first thing that we needed to do was to create a new column, "Years" that would hold all of the date-specific information for each campaign. To do this we used the Years() function, which took our "Date Created" column information, and converted it into simple year format. From there we were able to create a PivotTable that listed each campaign and the year that it was started. That, however, was far too broad for Louise's needs. We then added several filters into the PivotTable, so that Louise would only see relevant information, that is, the kickstarter campaigns that were dedicated to plays. We used the "Parent Category" to filter out all the other categories, leaving us with only the campaigns that were for plays. While this information was useful, perhaps to see if there were any trends year to year in how many campaigns were started, what we were really looking for was the success rate of these campaigns. In order to reflect only that data, we had to further separate the data into "Succesful", "Failed" and "Canceled" campaigns. These categories are tracked within the spreadsheet that Louise gave us, and we were able to make a column in our PivotTable that displayed the total number of campaigns that were successful, failed, or canceled and their respective start dates. We then altered the table to show only the month in which each campaign was started, so that Louise would be able to see which Month saw the most succesful campaigns. The image below displays the chart that we were able to make, using the data in our Pivot Table.
![Image of Analysis Based on Launch Date](https://github.com/Greg-Finin/kickstarter-analysis/blob/master/Outcomes%20based%20on%20Launch%20Date%202.0.png)

### Analysis of Outcomes Based on Goals
Louise's second request was that we anaylze the campaigns based on their goals. Did a high campaign goal have any effect on the success rate of the campaign? Did a low one? In order to do this we needed to create a series of dollar-amount ranges in which we could put our campaigns, to filter the data into a readable format. We created a new Worksheet within the excel file, with a column "Goals", that had various 'buckets' that we could put the campaigns into (Under $1000, Between $1000 and $4999, etc.). This allowed us to review each campaign based on their desired goal. From there, the challenging aspect of this project was to compile all the information and compare it to our new filters. We utilized the CountIfs() function, which was able to compare each theater campaign's target goal to the newly established column of dollar-amount ranges. Furthermore, we were able to use the same category we used above, that is the 'Outcomes' column, to display the number of successful, failed and canceled campaigns based on their target goal. From there it was a simple calcuation to get the percentage of succesful and failed campaigns based on their target goal, and to display that information in their own columns.The image below displays the chart that we were able to make, using the data in our Pivot Table.
![Outcomes Based on Goal](https://github.com/Greg-Finin/kickstarter-analysis/blob/master/Outcomes%20based%20on%20Goal%202.0.png)


### Challenges and Difficulties Encountered
As referenced above, the main challenges associated with these two projects were related to the gathering of specific metrics and key pieces of information. We were given a large datasets and requied to pare them down into concise, readable displays of relevant information. The diffuclty lay mostly in the filtering and sorting of the information, as improperly filtered data would provide Louise with results not relevant to her campaigns. If we were unable to create the columns such as 'Years' or 'Goals" and compare them directly to the dataset we were given, this task would have been far more difficult. In several cases we utilized excel functions that did most of the work, and if we were not familiar with such operations we would surely have encountered far more problems in the creation of this analysis.

## Results
- What are two conclusions you can draw about the Outcomes based on Launch Date?


It is clear from both the Table and the Graph, that in the years span that we are reviewing, May has more succesful campaigns than any other month, with 111. June, however, is not far behind, with 100, and actually has a higher rate of succesful campaigns. December, on the other hand, has the lowest number of succesful campaigns, with 37, and a very low rate of success, with 35 failed campaigns. 

- What can you conclude about the Outcomes based on Goals?


We can see from our Table that the Outcomes based on goals has a few stories to tell. The first being that, as one might expect, a low goal can mean a higher success rate, with the highest succes rate (76%) correlates to the lowest target goal (less than 1000). However, in reviewing the other portions of the table, we see that the two ranges $35000 to $39999 and $4000 to $4499 also have high success rates, 67%. This shows us that although the lowest target goal has the highest chance of being successful, a higher target goal does not impact the success rate in a drastic manner until you reach the $45000 and Greater than $50000 ranges.

- What are some limitations of this dataset?


This dataset is limited to campaigns that are only run on kickstarter. There have been far more theater productions funded by other methods, which this dataset does not address at all. 

- What are some other possible tables and/or graphs that we could create?


As mentioned above, a possible addition to this study could be a chart that displays the number of succesful campaigns per year. A downward trend in the success of campagins in the last few years might disuade someone from starting a new campaign. An upward trend, conversly, would encourage new campaigns.
