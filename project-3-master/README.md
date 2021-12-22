# Problem Statement:
As a Data Scientist I have been hired by Konami Holdings Corporation to find out when the best times to post announcements for their hit game, Metal Gear Solid as opposed to other big name video games. I created a predictive model that can look at subreddit posts and decide which key words are can distinguish which subreddit the post originated from. 


# Executive Summary
### I.Data Collection
   In order to successfully create a predictive model for classifying subreddit posts, there are several steps in my methodology. First, I collected subreddit data using pushshift.io API in order to extract the reddit post data and convert it into a data frame. I specifically used 5 batches of 100 posts during 2017-2021 for each of the subreddits r/metalgearsolid and r/Skyrim. This totaled to a dataframe of 1000 posts. I also filtered the posts by making sure they were relevant with comments and had a reddit score of greater than ten. Additionally I generated a column called "clean_title" which shows the reddit title posts in their lemmatized state. This makes finding certain patterns easier to identify. After generating the data, I exported it to a .csv file for later use.
### II.Data Cleaning and EDA
   Next I imported the data for cleaning and EDA. To clean I made sure to drop any null values. Since this data was self collected, their were only 7 null values found. I also engineered 2 additional columns. The first is "title_length" which shows the number of characters in the subreddit post. The other is "title_word_count" which showes the total words used in the subreddit posts. After that I made data frames of the subreddits individually in order to see which words were used most. After checking the descriptive statistics of the dataframe I found some of mean title_length was 56 characters and the mean title_word_count was 10 words. In the r/metalgearsolid it came as no suprise that "metal" and "gear" were the words that showed up the most.
### III.Preprocessing, Models, and Evaluation
   Finally I began running models on the data. First I created a baseline model with the variable "is_mgs" that had about a 50/50 split of subreddit posts. I incorporated several models including: LogisticRegression, MultinomialNB (Naive-Bayes), and RandomTreeClassifier. The words were preprocessed using the CountVectorizer and Tfidtvectorizer to be able to fit models to the words included. 
### IV. Conclusions
   After running several models with different parameters I was able to find some that worked better than others on predicting the right subreddit. The model that worked best was Model 6 which preprocesses with TfidfVectorizer and then fits to a RandomTreeClassifier. The results yielded a train score of 0.852, and test score of 0.803 which is a 30% increase from the baseline model. This model is unfortunately not very interpretable, but with the feature importances we can see which words are important in determining the classification of the the subreddits. The model falls short because the false negatives appear 34% of the time. However false positives only appear 5% of the time. This indicates that the model is more accurate in predicting the correct outcomes based on metal gear solid key words, but had trouble with predicting based on skyrim's key words.
Overall I would still recommend this model to be used to predict subreddit posts for metal gear solid to Konami in order to make announcements when the subreddit is highly active.














# Data Dictionary

| Feature     	| Type    	| Description                                                                                                                                                        	|
|-------------	|---------	|--------------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| subreddit   	| nominal 	| The subreddit names which are r/metalgearsolid and r/Skyrim.                                                                                                       	|
| title       	| nominal 	| The data pulled from the subreddits only including the subreddit post titles.                                                                                      	|
| is_mgs      	| nominal 	| Splits data set into a binary to find if the post originated from r/metalgearsolid. Assigned values are:<br>0 = Is Not Metal Gear Solid<br>1 = Is Metal Gear Solid 	|
| clean_title 	| nominal 	| The subreddit title posts but the words have been lemmatized to make the data easier to train on.                                                                  	|