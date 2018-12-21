---
Project 4 and 486 Final
---
#### Analysis
  I looked at Voter Turnout in the 2016 Presidential Election for Fairfax County, Virginia. I decided to first look at population distribution throughout the county. Dark green represents the most dense areas of people. I compared it to the voter turnout and noticed that generally, higher populations had lower turnout percentage. I looked at different city's voting turnout to see if there could be a correlation here. The biggest difference I noticed was that the average voting age was always significantly older than the average age of eligible voters. Even in Portland with a higher turnout percent had a difference of 4 years between averages. While Dallas with only 6% for the election for Mayor, voter turnout age had a difference of 21 years. While Fairfax County had a relatively high turnout it can be assumed that the more dense areas have more young people who often do not vote as much as their older counter parts who may live in suburban or rural areas. I did not factor in voting deserts becaues Fairfax is one of the richest counties in the United States and I do not believe it would be as big of a factor. 
  I then looked at voter data to see who they elected and normalized it with turnout data. I wanted to see if the candidate picked followed a trend. In figure 3, the blue values are areas with the highest turnout for Clinton while red were those who supported another candidate. Figure 4 is red where Trump was supported and blue was where another candidate was voted for. The data shows a trend for high population and low turnout was where Clinton had the most support and more rural areas had higher turnout. It is interesting to see despite lower turnout in the dense areas, Clinton still won 355,000 to 158,00 votes in the county with 82.5% turnout. In 2012 Obama beat Romney 315,000 to 207,000 votes with 80.5% turnout. This shows that generally Fairfax votes Democratically but it is interesting to see that despite Trump winning the presidential election, he did not have nearly as muchs support which calls into question the demographics and education of this county, to see if there are other factors leading to higher turnout against Trump.
  
[Figure 1]
![alt text](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/FinalProjectPop.png)
[Figure 2]
![alt text](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/voterturnout.png)
[Figure 3]
![alt text](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/FinalProjectClinton.png)
[Figure 4]
![alt text](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/FinalProjectTrump.png)

#### Methods
I used SQL to sort through most of the data. What was most important from what I downloaded were the results of the election and voter turnout. The 3rd SQL code helped me join the tables together. From the merged table I was able to use the field calculator to create new fields with the % Turnout - % Clinton/% Turnout and % Turnout - % Trump/% Turnout to get values for both Figure 3 and 4. For the population data I created hexagons and used the point data to fill each polygon and to get a sense for each value.
![](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/sql_1.png)
![](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/sql_2.png)
![](https://raw.githubusercontent.com/gkuykendall96/gkuykendall96.github.io/master/project4/sql_3.png)

##### Sources
http://www.whovotesformayor.org/compare
https://www.fairfaxcounty.gov/elections/sites/elections/files/assets/result/previous%20election%20results,%202010%20-%202018.pdf
Data from:  https://www.fairfaxcounty.gov/maps/open-geospatial-data
