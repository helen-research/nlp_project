# NLP Project - GitHub README files
The goal of this project is to use Natural Language Processing and a repository's README file to determine what the dominant programming language is for that repo. We did this by first scraping the information we needed from a little more than 700 of the most starred repositories. We normalized, cleaned, and stemmed/lemmatized the data, then we transformed the text data into a format that can be fed into a classification model. We created several transformations of the text data, including:
- tf-idf (TfidfVectorizer)
- bag of words (CountVectorizer)
- truncated singular value decomposition (TruncatedSVD) followed by one of the above transformations

