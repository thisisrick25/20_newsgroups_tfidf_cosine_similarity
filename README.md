# Questions

1. [Q1: 20 Newsgroups: TF-IDF and Cosine Similarity](#q1-20-newsgroups-tf-idf-and-cosine-similarity)
2. [Q2: IMDb: Text Preprocessing and Bag-of-Words](#q2-imdb-text-preprocessing-and-bag-of-words)
3. [Q3: IMDb: TF-IDF and Logistic Regression](#q3-imdb-tf-idf-and-logistic-regression)
4. [Q4: IMDb: Linear SVM](#q4-imdb-linear-svm)
5. [Q5: IMDb: Multinomial Naive Bayes and Logistic Regression](#q5-imdb-multinomial-naive-bayes-and-logistic-regression)

***

## Q1: 20 Newsgroups: TF-IDF and Cosine Similarity

Use the [20 Newsgroups dataset](https://www.kaggle.com/datasets/crawford/20-newsgroups), or another standard text-classification dataset of your choice.

Select **three categories** and randomly choose **100 documents from each category**.

1. Preprocess all selected documents by performing:
   - Lowercasing
   - Tokenization
   - Stop-word removal
   - Lemmatization
2. Convert all documents into **TF-IDF feature vectors**.
3. Select **two documents** and calculate their cosine similarity manually using **NumPy**, based on their TF-IDF vectors.
4. Implement the **cosine similarity calculation from scratch using NumPy**, without using any pre-built cosine-similarity function.
5. For **each document**, find its **five most similar documents** based on cosine similarity and report their corresponding classes.
6. Calculate and report:
   - Average similarity between documents belonging to the same class
   - Average similarity between documents belonging to different classes
7. Repeat the experiment using:
   - TF-IDF with **unigrams**
   - TF-IDF with **unigrams and bigrams**
8. Compare the results obtained from both representations. Discuss whether adding bigrams improves the ability of TF-IDF to identify documents belonging to the same class.
9. Present your final results in a comparison table and include at least five examples of document pairs with their cosine similarity scores and corresponding classes.

***

## Q2: IMDb: Text Preprocessing and Bag-of-Words

Load the [IMDb dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) and construct a complete preprocessing pipeline for the movie reviews.

**(a)** Convert the reviews to lowercase and use regular expressions to remove HTML tags, URLs, unnecessary punctuation, and other irrelevant characters.

**(b)** Tokenize the reviews and remove stop words.

**(c)** Apply lemmatization to the tokens. Compare the number of unique tokens before and after lemmatization.

**(d)** Implement your own function, `extract_word_features(review)`, that returns a dictionary containing the frequency of each word in a review.

> Do not use `CountVectorizer` for this part.

**(e)** Apply your function to the following reviews and display the resulting feature dictionaries:

```text
"This movie was absolutely amazing and entertaining"

"The movie was boring and predictable"
```

**(f)** Construct a Bag-of-Words representation of the dataset using `CountVectorizer`. Report the number of documents, number of unique features, and the shape of the resulting document-term matrix.

**(g)** Compare the vocabulary obtained before and after preprocessing. Identify words that disappear after preprocessing and explain, using the code output, why they were removed.

***

## Q3: IMDb: TF-IDF and Logistic Regression

Use the preprocessed IMDb reviews to build a sentiment classifier using TF-IDF features and Logistic Regression.

**(a)** Split the dataset into training and testing sets using an appropriate train-test split.

**(b)** Convert the reviews into TF-IDF vectors. Experiment with both unigram features and unigram-plus-bigram features.

**(c)** Train a Logistic Regression classifier using both representations.

**(d)** Report accuracy, precision, recall, and F1-score for both models.

**(e)** Plot the confusion matrix for the better-performing model.

**(f)** Compare the two models and determine whether adding bigram features actually improves sentiment classification.

**(g)** Use the predicted probabilities of Logistic Regression and evaluate the classifier using three different decision thresholds: **0.3**, **0.5**, and **0.7**. Report precision, recall, and F1-score for each threshold. Plot precision and recall values against the classification threshold.

**(h)** Identify five test reviews for which the model's predicted probability is closest to 0.5. Display the review, actual sentiment, predicted sentiment, and predicted probability.

**(i)** Examine these borderline cases and determine whether they contain ambiguity, negation, mixed sentiment, or other linguistic patterns that may make classification difficult.

***

## Q4: IMDb: Linear SVM

Use the same IMDb dataset and TF-IDF representation to build a sentiment classifier using a Support Vector Machine.

**(a)** Train a Linear SVM using `LinearSVC`.

**(b)** Experiment with at least four values of the regularization parameter:

$$C \in \{0.01, 0.1, 1, 10\}$$

**(c)** For each value of `C`, report the accuracy, precision, recall, and F1-score on the test set.

**(d)** Plot the F1-score against `C` and identify the value of `C` that gives the best test performance.

**(e)** Train a Linear SVM using:

1. Unigram TF-IDF features
2. Unigram-plus-bigram TF-IDF features

Compare the two models.

**(f)** Identify the ten most influential features for the positive class and the ten most influential features for the negative class using the learned SVM coefficients.

**(g)** Display these features together with their coefficient values.

> Investigate whether the most influential words make intuitive sense for sentiment classification.

**(h)** Find five reviews that the SVM classifies incorrectly but contain words that appear among its strongest positive or negative features. Display the reviews and analyse the possible reason for the error using the feature representation.

***

## Q5: IMDb: Multinomial Naive Bayes and Logistic Regression

Build a sentiment classifier using Multinomial Naive Bayes and compare its behaviour with Logistic Regression.

**(a)** Use the same training and testing split and the same TF-IDF feature representation used in Q2.

**(b)** Train a Multinomial Naive Bayes classifier.

**(c)** Report accuracy, precision, and F1-score, and display its confusion matrix.

**(d)** Train another Multinomial Naive Bayes model using Bag-of-Words features instead of TF-IDF features.

**(e)** Compare the following models:

| Model               | Features   | Accuracy | Precision | F1 score |
| :-: | :-: | :-: | :-: | :-: |
| Naive Bayes         | BoW        |          |           |          |
| Naive Bayes         | TF-IDF     |          |           |          |
| Logistic Regression | BoW/TF-IDF |          |           |          |

**(f)** Identify ten reviews on which Logistic Regression and Naive Bayes produce different predictions.

**(g)** For each model, calculate the probability assigned to the predicted class for these reviews. Investigate at least three disagreement cases in detail and use their words/features to determine why the two models may have produced different predictions.
