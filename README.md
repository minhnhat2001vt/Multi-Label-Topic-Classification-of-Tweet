# Multi-Label-Topic-Classification-of-Tweet
This is a group project in a Natural Language Processing (NLP) coursework, UEH university. The goal of this project is to build a NLP model that can label tweets under certain topics.
## Project overview
### 1. Data acquisition
- Using Tweepy, data are scrapped from Twitter from the following topics: 'Sony', 'politics', 'environment', 'technology', 'travel', 'sustainability', 'economy', 'social media', 'sport', 'music', 'photography', 'healthcare', 'education', 'Sony and politics', 'Sony and environment', 'Sony and technology', 'Sony and travel', 'Sony and sustainability', 'Sony and economy', 'Sony and social media', 'Sony and sport', 'Sony and music', 'Sony and photography'.
- Data then can be pickled into a new file and stored in the "Data.zip".
### 2. Data pre-processing
- Lowercase and remove punctuations from Tweets.
- Remove Stop Words.
- Tokenize words.
- Vectorize Tweet using TF - IDF technique.
### 3. Topic modelling
- Topics (Labels) are first binarized using MultiLabelBinarizer.
- Using Classifier Chain method to handle multi-label classification task, 20 classification chains were created. Each classifier chain contains a Naive Bayes model for each of the labels. Another 20 classification chains were created, this time is for the Logistic Regression model.
- The models in each chain are ordered randomly. In addition to the features in the dataset, each model gets the predictions of the preceding models in the chain as features. These additional features allow each chain to exploit correlations among the classes.
### 4. Model evaluation
- Metrics to evaluate models performance include: Recall, Precision and F1 Score.
