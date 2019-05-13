# NLP Project - GitHub README files
The goal of this project is to use Natural Language Processing and a repository's README file to determine what the dominant programming language is for that repo. We did this by first scraping the information we needed from a little more than 700 of the most starred repositories. We normalized, cleaned, and stemmed/lemmatized the data, then we transformed the text data into a format that can be fed into a classification model. 

We noticed that many of the actual programming languages can be found in the README files. For example, 'python' would be in the README of a repo that used Python because they are mentioning what program they are using. To account for this, we decided to make separate datasets that included the programming languages and those that didn't. This would allow us to see how big of a difference it made when including the programming language in the repo.

We created several transformations of the text data, including:
- tf-idf (TfidfVectorizer)
- bag of words (CountVectorizer)
- truncated singular value decomposition (TruncatedSVD) followed by one of the above transformations

We used four different types of classification models:
1. Logistic Regression
1. Decision Tree
1. Random Forest
1. KNN

Our models' performance varied depending on transformation and model type. Our best model was a logistic regression model using a bag of words as the features. It performed extremely well, giving 100% accuracy on the training set and 95% accuracy on the test set. 