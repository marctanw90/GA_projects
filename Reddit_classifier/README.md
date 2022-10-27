# Project 3 - Web APIs and NLP Classification


## Introduction

This project seeks to create a classification model to seperate posts drawn from two fairly similar subreddits. We'll use NLP to train a classifier on the two selected subreddits to predict which subreddit a given post came from. 

Reddit is a social news aggregation, content rating, and discussion website. Registered users submit content to the site such as links, text posts, images, and videos, which are then voted up or down by other members.

For this project, the two subreddits chosen are "CryptoCurrency" and "EtherMining". 2,000 posts per subreddit were scraped with the use of Pushshift API, a free API which allows the collection of text data from Reddit. Data cleaning and exploratory data analysis were performed to give an understanding of the data we collected with the API.

## Modelling & Results

The models were tuned using RandomizedSearchCV to save time to get a good working model. The results are shown in the table below.

|    Model     | train_score | test_score | generalisation |  f1_score | roc_auc_score |
|-------------:|------------:|-----------:|---------------:|----------:|---------:|
| cvec_rf |      0.8232|     0.7761 |           5.7258 |   0.8125   |          0.9096 |
| tfidf_rf |      0.8317 |     0.7867 |           5.4114 |   0.8181 |          0.9018 |
| cvec_logreg|  0.9729 |     0.8614 |          11.4665 |   0.8678 |          0.9414 |
| tfidf_logreg |      0.9402 |     0.8848 |           5.8914 |   0.8902 |          0.9544 |
| cvec_nb |     0.9086 |     0.8859 |           2.4960  |   0.8907 |          0.9427 |
| tfidf_nb |    0.91643  |     0.8827 |           3.6774 |   0.8834 |          0.9524 |

Classification models, unlike regression models have multiple metrics which results may be based on. 
Accuracy is used when the True Positives and True negatives are more important while F1-score is used when the False Negatives and False Positives are crucial. F1 score is usually handy for imbalanced datasets (as its calculated based on Precision and Recall). Lastly, for the area under curve of a ROC curve, it measures the usefulness of a test in general, where a greater area means a more useful test, the areas under ROC curves are used to compare the usefulness of tests. AUC metric measure performance for the classification problem at various threshold settings.

As we are not currently solving any specific problem statements and that we are dealing with a balanced dataset, the following considerations may be used in determining the "best" model.

* Highest accuracy score
* Best generalization score

## Conclusion
Form the results above, the most suited model for our specific classification task would be the Multinomial Naive Bayes with CountVectorizer model. It has the highest accuracy score and generalizes the best. It is worth noting
that though we have chosen the MultinomialNB model to be the best performer, it is nicknamed “naive” due to the fact that the model treats all words equally. It ignores grammar rules and common phrases.

However, there are definitely still things to consider especially in the event of a business setting: 

* AUC-ROC curve may not be the only indicator of finding the 'best' model when compared against other models.
* Different functions may look at different metrics prior to deciding on which model to implement to production. (e.g Marketing/Sales may focus on recall, whilst other functions may want to focus on precision etc)


## Recommendations:
* Better data cleaning via reggex to remove wallet addresses whilst retaining the graphics card specific numbers for example which are prevelant in ethermining subreddit would be good. As well as maybe having a spam filter to remove spam post which appear often in both subreddits. 
* We’re dealing with a balanced dataset. For imbalance dataset, class weights and over sampling techniques such as SMOTE may be implemented. F1 score could also come in handy for imbalanced datasets (as its calculated based on Precision and Recall).
* May consider testing out other models which may perform better for such a task specific to this project. Boosting techniques such as AdaBoost, Gradient Boost & XG Boost.