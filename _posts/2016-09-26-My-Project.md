

-----------------------------------------------------------------------





# Capstone Project: Probability of Accelerated Approval of Insurance Claims

Link to the jupyter notebook: [Probability of Accelerated Approval of Insurance Claims](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-capstone/part-05/Capstone_Final%20Report.ipynb)

Link to the presentation : [Capstone Slides](https://docs.google.com/presentation/d/19Ftz9oA0MKYr-654TIB_CI9ZXa3yUAVxh46qvcZz7js/edit#slide=id.p)

## Abstract

The data is from an insurance claims management company. The dataset is anonymized because it is a proprietory data to protect privacy. It has two categories of claims:

* claims that had an accelerated approval leading to faster payments
* claims for which additional information was required before approval could be made i.e. no accelerated approval was present

The train set contains the target column which has already been classified. The test set does not have the target column. In am attempt to figure out the best performing model, a train-test split of the train set has been performed.

An attempt has been made to fit different tree based models on the train set. Logarithmic loss function has been used to compare the performance of the models. It has been observed that Extra Tree Classifer with a few set of parameters had the best performance with a logloss value of 0.46. The Extra Tree Clssifier model has been used to make predictions on the test set.

## Problem Statement: 

When unexpected events happen, people expect their insurer to support them as quickly as possible. Claims management department at the insurer need to check several things before a claim can be processed and payments can be made. Data Science can play an important role in this sector and make claims processing faster and easier.

## Data Cleaning

The data has two parts: Train and Test set.

The train set has 133 columns in all. The 'target' column in the train set is the dependent variable which has been already been classified into 1 and 0 depending on whether the claims had an accelerated approval or not respectively. If the claim had an accelerated approval the 'target' value has been set to 1 and if the claim did not have an accelerated approval the target value has been set to 0.


The train set has 131 columns which are the variables either of categorical or numeric type. All string type variables are categorical. It has been mentioned that the dataset doesnot contain any ordinal variables. 

The test set contains 132 columns and does not have the target column. In this project, we would predict the  probability of each claim in the test set to have an accelerated approval.

## Discussion

* There is no fixed model that would perform equally well on every data set.
* In classification problem, performance of a model can be analyzed from the log_loss value and the ROC curve
* In this project, depending upon the log_loss value and the ROC curve, using the Extra Tree Classifier model is recommended.

-------------------------------------------------------------------------------------------------------------------------------------------------------

# Project 7: Airline Delay Analysis

Link to the jupyter notebook: [Airline Delay Analysis](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-07/starter-code/Airport%20Delay%20Analysis.ipynb)

The aim of this project is to analyze the operations of major airports around the country and trying to figure out the factors that cause departure and operational flight delays from 2004 to 2014. 

I intend to conduct PCA analysis to figure out the factors leading to delays in arrival and departure delays in the airports.

![](https://dpalit.github.io/images/project7_pairplot.png)

It can be observed from the above plot that there is a correlation between  'average airborne delay' , 'average gate departure delay’ and 'average taxi time out’. 

The following histogram plots of flight delays show that there is a positive skew in the distribution.

 ![](https://dpalit.github.io/images/project7_fig1.png)

![](https://dpalit.github.io/images/project7_fig2.png)

![](https://dpalit.github.io/images/project7_fig3.png)

The positive skew of 'average airborne delay' is relatively more compared to 'average gate departure delay' and 'average taxi time out'.

| Features | Person’s correlation co-efficient  |
|:-:|---|
| Average taxi time out + Average Airborne Delay	| 0.56 |
| Average Gate Departure Delay + Average Airborne Delay	| 0.4 |
| Year + Average Airborne Delay | -0.2 |

I would like to recommend FAA to invest in modernization because with the increase in modernization airlines delays are supposed to decrease.


-------------------------------------------------------------------------------------------------------------------------------------------------------

# Project 6: IMDB Movies Analysis

Link to the jupyter notebook: [IMDB Movies Analysis](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-06/project6_final.ipynb)

I have tried to gather the data using IMDBpy and have also taken help from a kaggle competition post.

In the IMDB movies data set there are a number of variables. I have filtered the data for English language and country as United States. In the new filtered dataset, the 'imdb-score' is the dependent variables and the independent variables are:  

budget i.e. the budget of the movie  

movie_facebook_likes i.e. facebook likes for the movie  

actor_2_facebook_likes i.e. facebook likes for the second actor  

actor_1_facebook_likes i.e. facebook likes for the first actor  

num_user_for_reviews i.e number of users for review  

num_voted_users i.e number of voted users  

gross i.e. the gross capital that the movies collected  

director_facebook_likes i.e facebook likes for the director  

duration i.e. duration of the movie  

## Parametric Model Analysis:

An attempt to figure out the linear co-relationship of the independent variables with the dependent variable has been done by doing scatter plots. It appears that "number of users for review", "number of voted users", "facebook likes for the movie" and "the gross capital" that the movies collected have no significant to very little linear relationship. The other variables donot exhibit any linear relationship.

The following plot shows a scatter plot between number of voted users and imdb_score.  

![](https://dpalit.github.io/images/project6_linear_plot.png)


## Non-Parametric Model Analysis

Hence, to figure out the features that are most important for the model, a non-parametric model has been built. A decision tree model has been made and using feature selection we determine the features that are more valuable to the model.

The score of the decision tree model is not very high and the variance is high. In an attempt to make a model with better score and low variance, we have done sample bagging and have used random forest regressor. Adaboost and gradient boost has also been performed. However, the model fit has improved only slightly.

The following plot describes the feature selection in random forest.  


![](https://dpalit.github.io/images/project6_feat_sel.png)

 
From feature selection, it can be observed that for the'imbd_score' the most influential features are the "number of voted users" followed by the "budget of the movie" and "duration of the movie". 

The suggestion to Netflix would be to collect the movies from the IMDB that have high "number of voted users", high "movie budget" and "duration" of the movie is also a factor to look into.  
  

------------------------------------------------------------------------------------------------------------------------------------------------------

# Project 5: Analysis of the Titanic Disaster


Link to the jupyter notebook: [Titanic Disaster Analysis](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-05/Project5_Final.ipynb)

Goal of the project: In this project we use the titanic passenger data (name, age, gender, social-ecominic status i.e. the PClass they were travelling in the ship) to predict who will survive the disaster and who will not survive the disaster. 
    
In the data, 'SibSp' represents Siblings and Spouse;
             'Parch' represents Parents and Childern;
              'PClass' represents the Passenger Class;
                'Survived' has binay value: 1 (survived) or 0 (not survived/ died);
                'Sex' has 1 (female) or 0 (male).
                
A logistic regression has been attempted to fit model to where 'Survival' is the dependent variable and 'Pclass',    'NewAge', 'Gender', 'Parch'and 'SibSp' are the dependent variables. It can be observed that when the value of the      Kneighbor = 7, the accuracy of the model is maximum at 0.75
    
![](https://dpalit.github.io/images/project5_KNN.png)
    
A logistic regression with scikit learn has been performed and the score of the model was 80%. 
    
From the co-efficients of the model, it appears that female passengers (co-efficient = 1.75) had the maximum chances of survival followed by passengers travelling in the first class (co-efficient = 1.48). 
People travelling in  the 3rd class and male passengers had lower chance of survival.
So, a female travelling in the first class had the most chances of survival.
    
Following is the confusion matrix that was generated from the regression:


| | predicted_survived | predicted_not_survived |
  |--------------------|------------------------|		
| survived  | 71 | 29 |
| not_survived | 22 | 146
 

From the above confusion matrix, we can see that the type II error is 29 and the type I error is 22. The type II  error means that a person who has infact survived, has been predicted not to have survived. So, the search is not on for that person.
    
Our goal is to reduce the type II error. The standard classification threshold for the above regression model was      0.5. By lowering the threshold to 0.06 the type II error was reduced to 1.  
    
Following is the ROC curve which is a plot between correct vs incorrect i.e. true positive rate vs false positive rate.
     
![](https://dpalit.github.io/images/project5_ROC.png)
    
Lasso and Ridge regularization were performed on the model followed by gridsearch. The best parameters for   gridsearch were C = 0.275 at penalty = 12.
     
Based on the model we have tried to predict the chances of survival of a male of age 26yrs with a family size of 2 and travelling on a second class ticket. The model has predicted that the chances of survival of the passenger as 21%.  
  

------------------------------------------------------------------------------------------------------------------------------------------------------

# Project 4: Salary Prediction for Data Professionals

Link to the jupyter notebook: [Salary Predictions for Data Professionals](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-04/project4_final.ipynb)

In this project we are trying to gauge the industry factors that influence the pay scale of professionals in the field of Data Science. This information is considered to be a valuable information for hiring firms. 

We used webscrapping methods to collect the salary information from the web, converted the data into csv and have imported the data using pandas into a dataframe.

The independent variables for the model are 'location' and 'job title'. The dependent variable for the model is 'pay' or 'salary of the individual'. Hence, according to the model, pay of an individual is influenced by the job title they hold and the location of their work. 

We have four work place locations: Boston, DC, New York, and San Francisco. We had a number of job titles in our original data which we have grouped into two buckets: Data Analyst and Data Scientist.


Classification model has been applied to the data by creating binary variables. Analysis has been performed by  Logistic regression using Statsmodel as well as scikit learn.

We have about 1110 rows of data for analysis. The following is the histogram of the pay(meanPay is the name of the column in the dataset) which presents the pay distribution.

![](https://dpalit.github.io/images/project4_histogram1.png)


The pay that is less than $20,000 has been considered as an outlier and has been removed from the dataset. The following histogram presents the pay distribution without the outliers.

![](https://dpalit.github.io/images/project4_histogram2.png)

The average pay has been calculate as $85,152.
The median pay has been calculated as $76,000.
Their is a standard deviation of 30048.

For binary classification, the cut of has been taken as 80,000. Pay less than 80K has been classified as low (denoted 0) and a pay above 80K has been classified as high (denoted 1).

The mean of the data is 44% i.e. 44% of the positions have  a pay above 80K.

In scikit learn, a model score of 81% has been obtained. 

The co-efficients of the model are:

| 0 | 1 | 
|:-:|---|
| DC | -0.052655 | 
| New York	| 0.05977 | 
| San Francisco | 0.95155 |
| Data Analyst | -3.5277 |
 
 
## Prediction: 

We tried to predict the salary of a Data Analyst in New York using the model.

The model predicted that the probability of finding a position as a Data Analyst in New York with a pay (high) i.e. over 80K is 20%.  
  

------------------------------------------------------------------------------------------------------------------------------------------------------

# Project 3: Market Analysis of Liquor Sales in Iowa

Link to the jupyter notebook: [Iowa Liquor Sales](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-03/project3_Iowa_Liquor_Sales.ipynb)

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
  
------------------------------------------------------------------------------------------------------------------------------------------------------


# Project 2: Bill Board Music Data Analysis 

Link to the jupyter notebook: [Bill Board Music Data Analysis](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-02/project_2.ipynb)


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
  

------------------------------------------------------------------------------------------------------------------------------------------------------


# Project 1: Summary of the SAT Scores in the United States

Link to the jupyter notebook: [SAT score Analysis](https://github.com/DPalit/GA-DSI/blob/master/projects/projects-weekly/project-01/starter-code/project_1.ipynb)

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
  







