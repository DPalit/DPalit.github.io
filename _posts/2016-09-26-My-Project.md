

# ** Project 1: Summary of the SAT Scores in the United States**

The data presents the mean Math and Verbal scores in 51 different states in the United States. United Sates has 50 states but DC has been included as a state in the data and that changes the number of states as 51. The last column with the state abbreviation  “ALL” is not a state ; hence has not been included in numerical analysis.

The data has four columns. The three columns with numeric values are “Verbal”, “Math” and “Rate”. The “State” column contains non-numeric value i.e. string type. 

In CSV, all data is in type string; however, if the dataset in loaded using pandas, the data type for the “State” column is object and the data type of the numeric columns is integer. The type of the data frame is object.

The minimum verbal score is 482 in DC and the maximum verbal score is 593 in IA. The minimum math score is 439 in OH and the maximum math score is 603 in IA.
The rate has a minimum value of 4 in three states SD, ND and MS. The rate has a maximum value of 82 in CT.

* The mean for math, rate and verbal is 531.84, 37 and 532.52 respectively.
* The median for math, rate and verbal 525, 33 and 527 respectively.
* The mode for math, rate and verbal is 499, 4 and 562 respectively.
* The standard deviation for math, rate and verbal is 35.92, 27.27 and 33.03 respectively.

The histograms for math, verbal and rate reveal that we have a non-normal distribution. In a normal distribution, the mean, median and mode values are the same. 
The scatter plot shows that the maximum math and verbal scores are at lower rates and as the rate increases, the math and verbal scores tend to drop. Hence the scores are inversely related to the rate.








# ** Project 2: Bill Board Data Analysis **



Bill Board is a music industry record chart for ranking the 100 most popular songs.

Assumptions: 

The data contains a number of empty spaces and stars (\*). I have replaced the empty spaces and the stars (\*) with 0.

The data presents twelve genres of music and 317 songs. If I assume that ‘R & B’ and ‘R&B’ as the same genre; there are 11 different genres of music in the data. 

Following are the different genres of music in the data:

| Genres | Number of songs in the genre |
|:-:|---|
|Rock	| 103 |
|Country	| 74 |
|Rap	| 58 |
|Rock ’n’ Roll	| 34 |
|R&B	| 13 |
|R & B	| 10 |
|Pop 	| 9 |
|Latin	| 9 |
|Electronica	| 4 |
|Gospel	| 1 |
|Jazz	| 1 |
|Reggae	| 1 |


![](https://dpalit.github.io/images/project2_barplot.png)

The genre ‘Rock’ is the most popular genre with 103 songs followed by ‘Country’ and ‘Rap’.

I have assumed that the column ‘time’ is the track time. The ‘time’ column in the data frame is of type string and I have extracted the integer values from the column for track time calculations. The histogram of track time shows that the maximum frequency distribution is at 4 i.e. maximum number of songs have a track length of around 4 minutes.


![](https://dpalit.github.io/images/project2_histogram.png)


| Statistical calculations | Values |
|:-:|---|
|Maximum Track Time	| 7.8 |
|Minimum Track Time	| 2.6 |
|Mean Track Time 	| 4.2 |
|Standard Deviation of Track Time	| 0.9 |


Among ‘Rock’ songs, “Where I Wanna Be” sung by “Jones, Donell” has the maximum track length of 6.22 minutes.

If we perform an analysis of the data we see that “Independent Women Part 1” achieved the no. 1 position in the bill board for 11 weeks. followed by Maria, Maria which was in the bill board for 10 weeks. Top two observations from the output has been given in the table below: 


| Songs in the no. 1 position | Number of weeks in No. 1 position |
|:-:|---|
|Independent Women Part 1 | 11 |
|Maria, Maria	| 10 |


I have tried to analyze for how many weeks a song has been in the top ten position in the bill board.
“Breadth” with a song index of 17 in the data frame sung by “Hill, Faith” belonging to the genre “Rap” has been in the top ten position for 19 weeks.
Top four observations from the output has been presented in the table below:


| Song in the top 10 position | Number of Weeks in top 10 position |
|:-:|---|
| Breathe | 19 |
|Maria, Maria	| 18 |
| Kryptonite	| 18 |
|Everything You Want | 18 |


So, we can observe that though “Independent Women Part 1” has been in the number 1 position for the most number of weeks (11 weeks) has actually been in the top ten position in the bill board for 16 weeks.

I have tried to analyze for how many weeks a song has actually been in the bill board. Top four observations from the output has been presented below:


| Song in the bill board | Genre | Number of Weeks |
|:-:|---|
|Higher	| Rock ’n’ Roll | 57 |
|Amazed	| Country | 55 |
|Kryptonite	| Rock | 53 |
|Breathe	| Rap | 53 |

So, we can observe that  even though ‘Higher’  was never in the number 1 position in bill board it has still been in the bill board for the longest period of time i.e. 57 weeks. ‘Kryptonite’ and ‘Breadth’ are among the songs to achieve the longest run as top ten and have also been in the bill board for relatively longer.

From the bill board data I would presume Breathe and Kryptonite to be the most popular songs because they have secured a position among the top ten for the most number of weeks along with being one of the longest runnings in the bill board.




# **Summary of Project 3 (Scenario 2)**

My model analysis is based on the 10% dataset of the Iowa liquor sales. The original data set is very large so I have chosen to work with 10% of the data set which covers the data from Jan 2015 to March 2016. The data had some missing values which the dataframe interpreted as NaN. I preferred to drop the NaN labels for regression analysis. So there is a possibility of some missing information.


The data had 270955 rows and 18 columns. In trying to figure out the columns (variables) that I could use in building the model for the data, it can be observed that:

* The data set had many categorical(qualitative) variables (columns)
* Some columns (variables) were related to other columns. For e.g.

    - "The State Bottle Retail" * "Bottle Sold" = "Sale (Dollars)" 
    - "Bottle Volume" * "Bottle Sold" = "Volume Sold (liters)" or "Volume Sold (gallons)"

* "Item Number" and "Item Description" relate to the same product.
* "Category" and "Category Name" relate to the same item.

I have chosen to build the model using quantitative variables. In my model, I have used Sale (Dollars) as the dependent variable and "State Bottle Retail", "Bottle Sold" and  "Bottle Volume (lts or gallon)" as independent variables. I have chosen to include "Zip Code" as an independent variable in my model. Including the "Zip Code", did increase the r2 value of the model and hence has affected the model fit.

**The top five county numbers that had the maximum liquor sales are as follows:**

| County Number | Sale (Dollars) | 
|:-:|---|
| 77 | 7.747219e+06 | 
| 57 | 3.139999e+06 |
| 82.0	| 2.457277e+06 |
| 52.0 | 2.077858e+06 | 
| 7.0 | 1.928017e+06 | 

From the data analysis, it appears that county number 77 had the maximum liquor sales in dollars followed by county number 57 and 82.

The top two Store Number in Iowa that had the maximum liquor sales are 2633 and 4829. They located in county "Polk" in county number 77 in the city of Des Moines.


**The location of the stores that had the maximum liquor sales can be presented using the following table:**

| Sale (Dollars) | Store Number | City | County | County Number |
|:-:|---|
| 1215399.02 | 2633 | DES MOINES | Polk | 77 |
| 1081941.88 | 4829 | DES MOINES | Polk | 77 |
| 531684.42	| 2512 | IOWA CITY | Johnson | 52 | 
| 504057.23 | 3385 | CEDAR RAPIDS | Linn | 57 |
| 398025.24 | 3420 | WINDSOR HEIGHTS | Polk | 77 |
  
In an attempt to figure out the **city that had the maximum liquor sales in the state of Iowa** the following table would be useful:    

| Sale (Dollars) | City | County | County Number |
|:-:|---|
| 4380886.26 | DES MOINES | Polk | 77 |
| 2486949.08 | CEDAR RAPIDS | Linn | 57 |
| 1697702.84	| DAVENPORT | Scott | 82 | 
| 1250666.19 | IOWA CITY | Johnson | 52 |
| 1211603.55 |  WATERLOO | Black Hawk | 7 |
| 1200607.02 | SIOUX CITY | Woodbury | 97 |  


It can be observed that Des Moines and Cedar Rapids are the two cities in Iowa that had the maximum liquor sales and are located in couty number 77 and 57 respectively. Couty number 77 and 57 were infact the top two counties with respect to maximum liquor sales in Iowa. 

The cities i.e. Davenport, Iowa City, Waterloo and Sioux City possess the counties that have recorded top liquor sales in State.

The following table presents a part of the output table in an effot to present the Cities and Counties that had **the maximum liquor volume sold in gallons and the state bottle retail price** for those locations. 

| Volume Sold (Gallons) | County Number | City | County | State Bottle Retail |
|:-:|---|
| 132747.24 | 77 | BONDURANT | Polk  | 17.24 |
| 132747.24 | 77 | WEST DES MOINES | Polk  | 39.36 |
| 132747.24	| 77 | GRIMES | Polk  | 16.49 | 
| 132747.24 | 77 | DES MOINES | Polk  | 9.78 |
| 132747.24 | 77 | DES MOINES | Polk  | 7.92 |
| 132747.24 | 77 | DES MOINES | Polk  | 24.24 |

![](https://dpalit.github.io/images/project3_timeplot77.png)

The above plot presents the liquor sale for the state of Iowa.

## Regression Analysis

A regression model for each county has been done with state bottle retail, volume sold and bottle sold as the independent variable and sale dollars as a dependent variable. The r2 value for county no 99 was 0.98 and the r2 value for county number 77 was 0.77.

A regression plot with four variables has been presented below. The r2 value for the model was 0.71

![](https://dpalit.github.io/images/project3_regression4.png)

![](https://dpalit.github.io/images/project3_predicted_actual.png)
 
I have used the lasso and ridge regularization; however, the r2 value remained nearly the same. After the cross value optimizationnon the lasso model the r2 value of the model increased to 0.77 and that was the best fit that I obtained for the model.

## Yearly sales prediction:

Based on the regression analysis and after analysis of the tables I would suggest opening stores in County Number 77.
County Number 77 had the maximum recorded liquor sales. In order to create a model for county number 77, I have chosen "Bottles Sold" and "Volume Sold (liters)" as my independent variables and "Sale (Dollars)" as my dependent variable.

The data for 2015 has been filtered for county number 77. The model has an r2 value of 0.99 which shows that the model has a good fit to the data.

I have taken the mean values of the independent variables for each store in an attempt to predict the yealy sales for each store in the county.

If we open a store in county number 77, I could predict that the yearly liquor sale for the store would be around 31,003 dollars. The average number of yearly bottles sold for the store could be predicted as  2298. The average volume of liquor sold for the new store has been predicted as 2007 liters. I could predict a price per bottle at the store as = 31003/2298 = 13.49 dollars based on the predictions of my model.

![](https://dpalit.github.io/images/project3_timeplotNew.png)

The above plot shows the yearly sale in couty number 77. My model predicts a yearly sale of around $31003 for each store which appears to be possible by observing the plot.

From all the above analysis, I would highly recommend opening stores in 77 number county in the state of Iowa.












