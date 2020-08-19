# Project 3: Web APIs & Classification

## Problem Statement  

It is election year for the United States of America, the Democratic nominee (Joe Biden) has open up to shortlisting companies capable of running analysis on social media platforms to inform his campaign of the public sentiments towards himself as well as his party [Source](https://www.nytimes.com/news-event/2020-election). His competition, President Trump has been utilising social media platforms; specifically twitter and has a higher presence in the digital space. On President Trump's own Facebook page, he has more than 29 million followers compared to Joe Biden's 2 million followers. Twitter tells a similar story; about 80 million for Trump, 5.4 million for Biden [Source](https://www.npr.org/2020/05/21/859932268/trump-and-biden-wage-an-uneven-virtual-campaign). 

As technology becomes intertwined with our daily living, it becomes inevitable that these platforms becomes more prominent in it influence for elections [Source](https://journalism.uoregon.edu/news/six-ways-media-influences-elections). Hence, it has become increasing important to understand the social media landscape to further improve one's chance when election day arrives. The campaign liaison has specified there are two categorise of competitions for companies to apply for tender. In the first category the model must be capable of classifying whether a block of text is generally democrat leaning or republican leaning. In the second category the model must be able to do sentiment analysis to understand if the block of text is positive or negative. Our team decided to focus on the first category.

We choose the reddit as our platform of choice and from there we would like to uncover the answers to the following problems:  

- **Between the two similar subreddits r/democrats and r/Republican are able to differentiate the post using Natural Language Processing models?**  
- **Which models is then likely to work best?**

Success is evaluated based on answering the problem statements and producing a model that has the highest classification score base upon metrics like accuracy, precision, recall and f1.   

## Executive Summary   

This project sets out to propose a classification modeling approach that would most accurately enable the us to predict which subreddit a post belongs to, using only the title and post data with subreddit names removed. This will assist in our application for the competition tender with the democratic nominee campaign. To illustrate this process and build a proposal using the selected platform Reddit, we have selected to build, evaluate, and compare classification models using Natural Language Processing (NLP) tools.  

Our chosen subreddits to compare are:

 - **r/democrats**
 - **r/Republican**   


#### Pre-Processing

Pre-processing includes stemming, lemmatizing, and vectorizing with Count Vectorizer and TF-IDF (Term Frequency-Inverse Document Frequency) to enhance modeling response. We divide our data into a Train and Test vector to begin modeling.

#### Model Selection

Using a GridSearchCV hyperparameter optimization, we selected 3 models to build and examine:
 - Multinomial Naive-Bayes
 - Random Forest
 - Logistic Regression  
 
## Conclusion and Recommendation

Based on our findings, we were able to answer the questions that we have formulated as part of the problem statement.  
- Between the two similar subreddits r/democrats and r/Republican are able to differentiate the post using Natural Language Processing models?    

Yes we were able to differentiate the post between the two different subreddits and compared to our baseline score of 50.025% we were able to improve it to 74.6%. However, due to the overlap nature of some major key words this has likely reduce the performance of our models.  
- Which models is then likely to work best?  

Multinomial Naive-Bayes model seems to works the best after evaluating the metrics for accuracy, precision, recall and f1-score across the 3 different models that were utilised. 

While we have managed to answer our problem statement that we have formulated, there is still room for improvement. Particularly in terms of the final selected model there is a huge different between the train and test score this is likely due to overfitting. We can take a few steps to further improve the model

1. Increase data size of collection by utilising pushshift.io which is an alternative reddit API that is capable of exceeding the 1000 post limit [source](https://pushshift.io/).
2. Collect additional text information like comments from the individual reddit post
3. Explore more alternative social media platforms like twitter or facebook