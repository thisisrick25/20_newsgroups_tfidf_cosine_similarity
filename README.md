# TF-IDF Text Classification and Cosine Similarity Experiment

Use the [20 Newsgroups dataset](https://www.kaggle.com/datasets/crawford/20-newsgroups) or another standard text classification dataset of your choice.

Select **three categories** and randomly choose **100 documents from each category**.

## 1. Data Preprocessing

Preprocess all selected documents by performing the following steps:

- Lowercasing
- Tokenization
- Stop-word removal
- Lemmatization

## 2. TF-IDF Feature Extraction

Convert all preprocessed documents into **TF-IDF feature vectors**.

## 3. Manual Cosine Similarity

Select **two documents** and calculate their cosine similarity manually using **NumPy**, based on their TF-IDF vectors.

## 4. Cosine Similarity from Scratch

Implement the **cosine similarity calculation from scratch using NumPy**.

Do **not** use any pre-built cosine similarity function.

## 5. Most Similar Documents

For **each document**, find its **5 most similar documents** based on cosine similarity.

For each retrieved document, report its corresponding class.

## 6. Similarity Analysis

Calculate and report:

- The **average similarity between documents belonging to the same class**
- The **average similarity between documents belonging to different classes**

## 7. Compare Unigrams and Bigrams

Repeat the complete experiment using both:

### A. TF-IDF with Unigrams

Use individual words as features.

### B. TF-IDF with Unigrams and Bigrams

Use both individual words and two-word sequences as features.

## 8. Comparison and Discussion

Compare the results obtained from the two representations.

Discuss whether adding **bigrams improves the ability of TF-IDF to identify documents belonging to the same class**.

Base the discussion on the experimental results.

## 9. Final Results

Present the final results in a **comparison table**.

Also include **at least 5 examples of document pairs**, reporting for each pair:

- Document 1
- Class of Document 1
- Document 2
- Class of Document 2
- Cosine similarity score

The final submission should clearly present the methodology, results, comparison between unigrams and unigrams + bigrams, and the resulting discussion.
