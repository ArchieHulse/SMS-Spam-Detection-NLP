# SMS Spam Detection NLP

<p align="center">
  <img src="NLP%20Image.jpeg"
       alt="SMS Spam Detection using Natural Language Processing"
       width="850">
</p>

## Project Overview

# SMS Spam Detection NLP

<p align="center">
  <img src="NLP Image.jpeg"
       alt="SMS Spam Detection using Natural Language Processing"
       width="900">
</p>

# SMS Spam Detection using Natural Language Processing

**Author:** Archie Hulse  
**Project:** MSc Data Science — Natural Language Processing  
**Dataset:** SMS Spam Collection v.1 (5,574 labelled messages)

## Overview

This project investigates how text preprocessing, semantic representations and traditional machine-learning classifiers can be applied to SMS spam detection. It uses the SMS Spam Collection dataset, containing messages labelled as `spam` or `ham` (legitimate).

The workflow covers:
- Exploratory analysis of the message corpus and class distribution.
- Comparison of minimal and more extensive text preprocessing.
- Word2Vec embeddings to explore semantic relationships between words.
- Naive Bayes and Logistic Regression text classification.
- Model evaluation and error analysis, with attention to the imbalanced class distribution.

## Methods

### Text preprocessing
Two preprocessing approaches are compared:
- **Minimal:** lowercasing and tokenisation.
- **Maximum:** lowercasing, tokenisation, removal of punctuation/numbers and stopwords, and lemmatisation.

### Word embeddings
A 50-dimensional Word2Vec model is trained on the preprocessed messages (window size 5, minimum word count 5). PCA is used to visualise selected spam-related terms and their nearest neighbours.

### Classification
The notebook trains and compares:
- Multinomial Naive Bayes
- Logistic Regression

The classification code vectorises the preprocessed messages using `CountVectorizer` (bag-of-words). Word2Vec is explored separately for semantic representation and visualisation.

### Evaluation
Models are evaluated using accuracy, spam precision, spam recall, F1-score and confusion matrices. The notebook also examines misclassified examples and false negatives.

## Repository structure

```text
SMS-Spam-Detection-NLP/
├── data/
│   └── SMSSpamCollection
├── notebooks/
│   └── SMS_Spam_Detection.ipynb
├── report/
└── requirements.txt
```

## Getting started

1. Clone this repository.
2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open `notebooks/SMS_Spam_Detection.ipynb` in Jupyter.
4. Run the notebook from top to bottom.

The notebook downloads the required NLTK resources when run.

## Requirements

Python 3.10+ is recommended. See `requirements.txt` for the Python packages used.

## Dataset and attribution

The SMS Spam Collection v.1 was created by Tiago A. Almeida and José María Gómez Hidalgo, with contributions from the NUS SMS Corpus. The dataset contains 5,574 English-language messages: 4,827 legitimate messages and 747 spam messages.

Please cite the dataset and its associated publication when using it:

- Almeida, T. A., Gómez Hidalgo, J. M., & Yamakami, A. (2011). *Contributions to the Study of SMS Spam Filtering: New Collection and Results*. Proceedings of the 2011 ACM Symposium on Document Engineering.
- UCI Machine Learning Repository: [SMS Spam Collection](https://doi.org/10.24432/C5CC84).

The dataset's accompanying documentation requests attribution to the original authors and source. See `data/README_dataset.txt` for the original dataset documentation.

## Notes

This is an academic portfolio project. The results are based on the supplied dataset and train/test split; they should not be interpreted as evidence of performance on contemporary SMS traffic without further validation.
