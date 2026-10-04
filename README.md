# 20_newsgroups_tfidf_cosine_similarity

Use the 20 Newsgroups dataset or another standard text classification dataset of your choice. Select three categories and randomly choose 100 documents from each category.

Preprocess the documents by performing:
Lowercasing
Tokenization
Stop-word removal
Lemmatization
Convert all documents into TF-IDF feature vectors.
Select two documents and calculate their cosine similarity manually using NumPy based on their TF-IDF vectors.
Implement the cosine similarity calculation from scratch using NumPy, without using any pre-built cosine similarity function.
For each document, find its 5 most similar documents based on cosine similarity and report their corresponding classes.
Calculate and report:
Average similarity between documents belonging to the same class
Average similarity between documents belonging to different classes
Repeat the experiment using:
TF-IDF with unigrams
TF-IDF with unigrams and bigrams
Compare the results obtained from both representations and discuss whether adding bigrams improves the ability of TF-IDF to identify documents belonging to the same class.
Present your final results in a comparison table and include at least 5 examples of document pairs with their cosine similarity scores and corresponding classes.
