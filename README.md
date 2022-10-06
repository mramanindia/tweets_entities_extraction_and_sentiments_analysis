# Tweets Entities Extraction and Sentiments Analysis

### Note:

This Notebook Aims to solve two objectives:
* Objective 1: Extracting and counting most frequent entities from the tweets.
* Objective 2: Finding the sentiment/polarity of each author towards each of the entities. 


Technology used: Natural Language Processing, Data Pre-processing, Sentiment Analysis, Entities Extraction, TextBlob library, Google Translator API and others.

The Approach of the objectives are well elucidated and have clear Visualization for better Insights into the working of each notebook cell.

\
I hope you will love the approach and the presentation of the solution.
\
Thanks & Regards,\
Aman India.

\
**My handles**
> LinkedIn: https://www.linkedin.com/in/mramanindia/
\
> Github: https://github.com/mramanindia
\
> Mail: amanindiamuzz@gmail.com
\
> Kaggle: https://www.kaggle.com/amanindiamuz

<a href="https://www.youtube.com/watch?v=sw0NrYbK5RI"><img src="https://i.ibb.co/MNcw5Cj/Blue-and-Yellow-Gradient-Meditation-Youtube-Thumbnail.png" alt="Tweets_entity_extraction_and_sentiment_analysis" border="0" /></a>



## Video Explanation: https://youtu.be/sw0NrYbK5RI

# The Approach (Solution)
The Approach for this problem statement is more leaned toward Data Preprocessing. (Cleaning data and removing Unnecessary elements from it.)
Useless elements: Emojis, URL links, and others.

## **Steps involved in solving the Objectives are:**
1.  Raw data Analysis
2.  Conversion of Raw data to Dataframe
2.  Defining functions for future uses
4.  Translating Tweets to the English language
3.  Data Pre-processing (Cleaning Tweets)
    * Finding text with spaces
    * Numbers in the tweets
    * URL Link
    * Hashtags
    * Emojis
    * Word less than 2 character
    *  And others...

4.  Extracting Entities from the tweets with their frequency
5.  Data Visualization
7.  Solution of Objective 1 (done)
8. Authors' sentiment analysis through tweets
10. Solution of Objective 2 (done)


### Here are all the steps in detail:
### --> Raw Data Analysis
Raw data analysis is one of the core parts of the solution-building process as it helps in understanding the problem statement in a better way and extracting the idea for building the Skelton of Ideology.

Moreover, it helps in finding out, major issues in the data that needed to be rectified in the data cleansing process.

### --> Conversion of Raw data into dataframe
For getting started with the Approach, The main thing is putting data into the mold.\
Over here,
Conversion of the Raw data(Tweets) into pandas data frame is the process.

### -->  Defining Functions for future uses

For Optimality, defining functions in the earlier steps helps in Better Implementation.

### --> Translating tweets into English Language
```
.apply(translator.translate, src='ja', dest='en')
```

During the Data analysis process, some tweets were in the Japanese language.

Thus, to get the best out of the data, Conversion of Japanese tweets into the English Language was Important.
With use of Google translate API, It can be done.

### --> Data Pre-processing

Data Pre-Processing is one of the critical tasks. There was a ton of debris in the data, and cleaning and identifying them is one of the major tasks.

After cleaning useless elements, All the cleaned data is inserted into column name "clean_tweet", 

### --> Extracting Entities and counting its frequency

Extracting Entities is one of the big Challenges, There are various methods avilable to extract the entities, Like "tokenization", and "Stemming". But those are limited to the words.

In tokenization there needed to fix a word count for extracting entities, but for this problem statement, There needed the entities of dynamic length. 
Entities that give the main idea of the tweets.

Thus with the use of TextBlob library's  "Noun_phrase extractor", Entities of the Tweets were extracted.

### --> Data Visualization

Visualizing the Entities and their count using graphs for better insights.

### --> Objective 1 Soluction

For completing objective 1, I created a new data frame with the entities and their frequency count in descending order.

Put the file location and with help of the to_csv function, saved it in the directory.

### --> Authors sentiments analysis through its tweets

This is also one of the challenging Data Engineering and Research based task,
First I created a copy of the Data frame of, "Clean_tweet", "Author", and "Entities".

Then the task was tagging all the tweets entities of the user in one row.

After then, I worked with the NLTK sentiment analysis package where I put the percent of sentiment towards Negtiveness, Postivness, and Neutral of the author.
Thus, made a new column and put the leading Sentiment in that.

### --> Soluction of Objective 2

As for building the solution of objective 1, I made a new data frame and with the help of the to_csv function, saved the data frame in CSV file to the directory.


### **Conclucion:**

Data Cleansing and Entities Extraction were a crucial parts of the solution. Removing unnecessary elements makes tweets ready for further processes, and This part of the process consumes most of the time.

After then, Entities Extraction is a key point in the solution. Finding the right entities defines extracting the right phrases from the tweets on which the core meaning of tweets relies on.

Then, there comes extracting the sentiments of each entities from the tweets with the help of "NLTK package SentimentIntensityAnalyzer" and there is the end of the soluction.







