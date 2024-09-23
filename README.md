# Gender_Identification_From_TWEET
Data Set -https://www.kaggle.com/datasets/crowdflower/twitter-user-gender-classification/code

# Summary:-
Cleaning Dataset:
•	Unnecessary columns like, '_unit_id', '_last_judgment_at', 'user_timezone', 'tweet_coord', 'tweet_count', 'tweet_created', 'tweet_id', 'tweet_location', 'profileimage', 'created' were dropped.
•	Rows with unknown gender and no gender were removed.
•	Profile attributes- 'profile_yn', 'profile_yn:confidence', 'profile_yn_gold' were removed as they were unavailable.
•	Rows with confidence of labeling gender<100% were removed.

# Manipulating Text Data:
•	Text was normalized-(everything was converted to lower case, and URLs, special characters and double spaces were removed.
•	The most common words which were meaningless in terms of sentiment (called stopwords) were removed.

# Lemmatization:
•	Words which expressed same positivity were reduced to their roots using Porter algorithm.
•	Two tokenizers, a regular one and one that performs steaming, were used to break down the tweets into individual words.

# Exploratory Data Analysis: 
The answers to the following questions were explored: 
1)	What are the most common emotions/words used by Males and Females? 
Most common words used by:
a)	Females- im, like, get
b)	Males- like, get, im
c)	Brands- weather, get, updates
2)	Which are the most frequently used link colours by Males amd Females?
Most frequently used link colours by:
a)	Males- 0084B4, 009999, 3B94D9
b)	Females- 0084B4, 9266CC, F5ABB5

# Visualization:
1)	A countplot was created to visualize the amount of each Gender.
2)	A bar plot was created to visualize the amount of retweets.
3)	A bar plot was created to visualize colors attributes.

# Classification models with Tweet-text only:
	Independent variables- Text, Description.
	Dependent variable- Gender.
Firstly, the categorical labels were converted into numerical ones and it was encoded using LabelEncoder. The data was split into train and test.
•	Logistic Regression Model:
	Accuracy obtained- 59.99517141477547%
•	Random Forest:
	Accuracy obtained- 56.76001931434089 %
•	SVM:
	Accuracy obtained- 59.82617093191694 %
	Best Accuracy: Logistic Regression Model
Classification models with content of Description added to text:
To increase the accuracy further the ‘description’ was concatenated with ‘text’ and training dataset was re-created.
•	Logistic Regression Model:
	Accuracy obtained- 68.15548044422984 %
•	Random Forest:
	Accuracy obtained- 64.48575567358764 %
•	SVM:
	Accuracy obtained- 68.68662481892805 %
          Naive Bayes Gave Accuracy of 69. .48575562984
Best Accuracy: Naïve Bayes
Ensemble Modelling:
Ensemble technique was used to take advantage of all the three models.
	Accuracy obtained: 69.97633993239981 %

# Conclusion:
The results show that the Tweet text  yields a moderate accuracy, but with the content from the Description, the performance of classification models significantly improves yielding much better accuracy.
Implementing Ensemble Modelling slightly increases the accuracy.

