# TF-IDF Text Classification and Cosine Similarity Experiment

Use the [20 Newsgroups dataset](https://www.kaggle.com/datasets/crawford/20-newsgroups) or another standard text classification dataset of your choice.

Select **three categories** and randomly choose **100 documents from each category**.

1. Preprocess all selected documents by performing:

- Lowercasing
- Tokenization
- Stop-word removal
- Lemmatization

2. Convert all documents into **TF-IDF feature vectors**.

3. Select **two documents** and calculate their cosine similarity manually using **NumPy**, based on their TF-IDF vectors.

4. Implement the **cosine similarity calculation from scratch using NumPy**, without using any pre-built cosine similarity function.

5. For **each document**, find its **5 most similar documents** based on cosine similarity and report their corresponding classes.

6. Calculate and report:

- Average similarity between documents belonging to the same class
- Average similarity between documents belonging to different classes

7. Repeat the experiment using

- TF-IDF with **unigrams**
= TF-IDF with **unigrams and bigrams**

8. Compare the results obtained from both representations and discuss whether adding bigrams improves the ability of TF-IDF to identify documents belonging to the same class.

9. Present your final results in a comparison table and include at least 5 examples of document pairs with their cosine similarity scores and corresponding classes.
