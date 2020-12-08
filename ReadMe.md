# Do Business Owners Care About Politics(the README.ipynb has all the graphs correctly visualized)

## Motivation
  My main interest in this topic came from the recent 2020 election, how it seemed to take over everyones news and media and seemed to have a disproportionate impact on everyones lives. What I was interested in though was to what extent do Americans actually fear the results, the instability that shifts in power cause, and what impact do elections have on the public mindset. To test these questions I decided to analyze data on new business that where announced. This focus on new businesses being created is supposed to represent Americas mentality as a whole and how confident they are in starting new and risky endevours. As if the political climate is as disruptive and choatic to Amercian life as we are lead to believe then there should be a reduction of new business being born in fear of the election.

## Data Sources
  My source was the census.gov website that has information like how many businesses applications where inputed each week for the past 14 years. There are a couple of categories of new business applications but I mainly focused on the overall vallues and their changes. 

## Cleaning
  The first thing I cleaned up was I made was I made a data file with just the total business applications on ellection years, as well as the year leading up to the election to act as a baseline. I also used the data that compared changes from the same week of the previous year to analyze the changes of the differences between years on election years vs the year prior. To analyze a more general view on the applications I also created a file with all non ellection year data and a seperate file with all election year data. I had to remove the recent 2020 election as the data was too much of an outlier and wouldnt represent the normal election year as there was a masive spike in applications. The final dataset I created was a file with all the differences between year data for election years and non election years. This dataset had 2 outliers that I had to remove, week 1 in 2013 and week 2 in 2015 as they where more than 5x the average percent change for other weeks,  
https://www.census.gov/econ/bfs/csv/naics2.csv

## Visualization

### Year-Year Comparisons
First I started by graphing total business applications on election years and the years prior:
![image.png](attachment:image.png)
![image-2.png](attachment:image-2.png)
![image-3.png](attachment:image-3.png)
![image-4.png](attachment:image-4.png)

### Analysis
There was no clear difference(exept for the aforementioned 2020 election year). So I compared the total yearly business applications:

Bush           2668870.0

Bush_Obama     2545470.0

Obama1         2547520.0

Obama_Obama    2547520.0

Obama2         2795320.0

Obama_Trump    2948570.0

Trump          3487560.0

Trump_         4026060.0

This was still inconclusive as some election years had increases, like the 2016 election and other had dicreases like the 2008 election.

### Year-Year Percentage Changes
There didnt apear to be any huge differences between comparing election year data and non election year data so I moved on to compare the changes between years, so the total shift in percentages between 2006-2007 compared to the shift in percent in 2007-2008:
![image.png](attachment:image.png)
![image-2.png](attachment:image-2.png)
![image-3.png](attachment:image-3.png)
![image-4.png](attachment:image-4.png)

### Analyzing
These visualasations also showed no clear trends of any difference betweeen election years and non election years(exept for the aforementioned 2020 election). I then compared total percantage changes between years to see if there was any differences:

Bush             31.40

Bush_Obama     -153.86

Obama1          173.38

Obama_Obama       8.69
 
Obama2          622.33

Obama_Trump     327.53

Trump            29.77

Trump_         1266.72

This comparison showed (When not taking into account the 2020 election) an average total drop of 215% percentage points which points to a dicrease in growth during election years. 

### Further Analysis
To furthyer analyze the data I combined total business applications on election years and non election years and compared the regression lines between the graphs:
![image.png](attachment:image.png)
![image-2.png](attachment:image-2.png)


Comparing thje reggreesion coefecents shows a dicrease in reduced ghrowth throughout the year with the election years dicreasing by -288 and the non election years dicreasing by -323. So this data would contradict my first analysis but it can be explained by the fact that there are more data points in the non election data that includes recesion numbers where there was a dicrease in business applications. 

### Why I Removed The 2020 Election
Analyzing the trend during the 2020 election makes clear why I removed it from most analysis as the data showed a speratic increase in applications throughout the year:
![image.png](attachment:image.png)
Which has a regression line that increases by 579 through the year, which is completely out of the norm when it is compared to other election years.

## Final Analysis
To complete my analysis I ploted all the percent changes between years of non election data and election data to see how the overall growth changed between election year and non election year:
![image.png](attachment:image.png)
![image-2.png](attachment:image-2.png)
These data plots had almost identical regreasion lines with the election years changes in percentres regresion line increasing by lesss than .019% through the year and non election percentage changes through the year reggresion line change by .025%.

Note: This final analysis does not include 2020 election data as its regresion line shows it is an outliar compared to other election years. I also removed 2 data points in the non election data(2013 week 1 and 2015 week 2) as their values are more than 5 times the normal change in percentage.

## Final Conclusions
The Final analysis shows that there is no clear correlation between election year changers in percent and non election year changes in percent. This analysis could be flawed however as when you analyze individual years there apears to be a corelation with a dicrease in percentage growth and election year, hinting that to some degree elections have a negative effect on the confidence of the public in their economic security and opportunity. This flaw in the analysis comes from the 2008 reccesion and the slow initial growth that came after it resulting in drastically different results between the growth leading up to each election meaning a trend can not be extrapulated from just the effect of these 4 elections on Business Growth.

### Descriptions of Code and Materials
The data is organized as follows:

YearlyValues.csv-Includes total data for election years and the year prior.

Difference_year.csv - Inlcudes percent changes for election years and the year prior.

TotalValues.csv-Includes the combined total of applications on non election years.

TotalElection.csv-Includes the combined total of applications on election years.

TrumpRe.csv-Includes the total business applications on 2020.

TotalDiff.csv-Includes the total differences in percent between non election year data.

TotalDiffElection.csv-Includes thje total percentage changes on election years.



```python

```
