# TF-IDF Text Classification and Cosine Similarity

Use the **20 Newsgroups dataset** ([Kaggle](https://www.kaggle.com/datasets/crawford/20-newsgroups)) or another standard text-classification dataset of your choice.

Select **three categories** from the dataset and randomly select **100 documents from each category**, resulting in a total of **300 documents**.

## Tasks

### 1. Text Preprocessing

Preprocess all selected documents by performing the following operations:

- Lowercasing
- Tokenization
- Stop-word removal
- Lemmatization

### 2. TF-IDF Representation

Convert all preprocessed documents into **TF-IDF feature vectors**.

### 3. Manual Cosine Similarity

Select any two documents and calculate their cosine similarity manually using **NumPy** based on their TF-IDF vectors.

Show the calculation using:

\[
\text{Cosine Similarity}(A,B)
=
\frac{A \cdot B}
{\|A\|\|B\|}
\]

### 4. Cosine Similarity from Scratch

Implement the cosine similarity calculation from scratch using **NumPy**.

Do **not** use any pre-built cosine similarity function such as `sklearn.metrics.pairwise.cosine_similarity`.

### 5. Most Similar Documents

For **each document**, find its **5 most similar documents** based on cosine similarity.

For each retrieved document, report:

- Document identifier
- Cosine similarity score
- Class/category of the original document
- Class/category of the similar document

### 6. Same-Class vs. Different-Class Similarity

Calculate and report:

- The **average cosine similarity between documents belonging to the same class**
- The **average cosine similarity between documents belonging to different classes**

### 7. Compare Unigrams and Bigrams

Repeat the complete similarity experiment using the following two TF-IDF representations:

#### A. Unigrams
Use only individual words as features.

#### B. Unigrams + Bigrams
Use both individual words and two-word sequences as features.

### 8. Analyze the Effect of Bigrams

Compare the results obtained using unigrams with those obtained using unigrams + bigrams.

Discuss whether adding bigrams improves the ability of TF-IDF to identify documents belonging to the **same class**.

Support the discussion using the calculated similarity values.

### 9. Final Results and Examples

Present the final results in a **comparison table** containing, at minimum:

| Representation | Average Same-Class Similarity | Average Different-Class Similarity |
|---|---:|---:|
| TF-IDF Unigrams | | |
| TF-IDF Unigrams + Bigrams | | |

Also include **at least five examples of document pairs**, showing:

- Document 1
- Class of Document 1
- Document 2
- Class of Document 2
- Cosine similarity score

## Expected Deliverable

Submit a Jupyter Notebook containing:

1. Dataset selection and sampling
2. Text preprocessing
3. TF-IDF feature extraction
4. Manual cosine similarity calculation
5. NumPy implementation of cosine similarity
6. Top-5 similar documents for every document
7. Same-class and different-class similarity analysis
8. Unigram experiment
9. Unigram + bigram experiment
10. Comparison table
11. At least five document-pair examples
12. Discussion of whether bigrams improve same-class document identification
