

## ** Project 1: Summary of the SAT Scores in the United States**

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








## ** Project 2: Bill Board Data Analysis **


Bill Board is a music industry record chart for ranking the 100 most popular songs.

Assumptions: 

The data contains a number of empty spaces and stars (*). I have replaced the empty spaces and the stars (*) with 0.

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

The genre ‘Rock’ is the most popular genre with 103 songs followed by ‘Country’ and ‘Rap’.

I have assumed that the column ‘time’ is the track time. The ‘time’ column in the data frame is of type string and I have extracted the integer values from the column for track time calculations. The histogram of track time shows that the maximum frequency distribution is at 4 i.e. maximum number of songs have a track length of around 4 minutes.

|Maximum Track Time	| 7.8 |
|Minimum Track Time	| 2.6 |
|Mean Track Time 	| 4.2 |
|Standard Deviation of Track Time	| 0.9 |

Among ‘Rock’ songs, “Where I Wanna Be” sung by “Jones, Donell” has the maximum track length of 6.22 minutes.

If we perform an analysis of the data we see that “Independent Women Part 1” achieved the no. 1 position in the bill board for 11 weeks. followed by Maria, Maria which was in the bill board for 10 weeks. Top two observations from the output has been given in the table below: 


| Song in the no. 1 position | Genre | Number of Weeks |
|:-:|—|—|
|Independent Women Part 1 | Rock | 11 |
|Maria, Maria	| Rock | 10 |

I have tried to analyze for how many weeks a song has been in the top ten position in the bill board.
“Breadth” with a song index of 17 in the data frame sung by “Hill, Faith” belonging to the genre “Rap” has been in the top ten position for 19 weeks.
Top four observations from the output has been presented in the table below:


| Song in the top 10 position | Genre | Number of Weeks |
|:-:|—|—|
|Breathe	| Rap | 19 |
|Maria, Maria	| Rock | 18 |
|Kryptonite	| Rock | 18 |
|Everything You Want	| Rock ’n’ Roll | 18 |

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






