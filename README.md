# Corpus Analysis - Superheroes vs. Horror

## Overview

This project analyzes text documents from two categories: Superheroes (Avengers) and Horror (Drag Me to Hell). The analysis includes:

Bag-of-Words (BoW) Representation

Log-Likelihood Ratios for Top 10 Words

Naïve Bayes Classification

Latent Dirichlet Allocation (LDA) Topic Modeling

Topic Distribution Analysis

## Directory Structure

```
project_directory/
│── output/
│   ├── avengers/          # Folder containing Avengers-related text files
│   ├── drag_me_to_hell/   # Folder containing Horror-related text files
│── main.py                # Main script to execute the analysis
│── README.txt             # This file
│── requirements.txt       # List of required Python libraries
```

## Setup Instructions

## 1. Install Dependencies

Ensure you have Python 3 installed. Install required dependencies using:
```
pip install -r requirements.txt

This will install:

nltk

numpy

pandas

gensim

sklearn
```
Additionally, download necessary NLTK resources:
```
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
```
## 2. Run the Analysis

Execute the main script:

homework2_nl3.ipynb

This will:

Load and preprocess the text documents.

Compute and display the top 10 most frequent words per category with log-likelihood ratios.

Train a Naïve Bayes model and extract category-specific words.

Perform LDA topic modeling, assigning unique labels to each topic.

Compute the top 3-5 topics per category based on document distributions.

## . Expected Output

The script will print:

Top 10 Words for Each Category (With Log-Likelihood Ratios)

LDA Topic Modeling Results (25 words per topic)

Average Topic Distribution per Category

Top 3-5 Most Representative Topics for Each Category

Example output:

Top 10 words for Superheroes:
  Word      Log-Likelihood Ratio
  agent               4.823533
  man                 1.807733
  iron                2.818515
  captain             4.317113
...
==================================================

## Top Topics for Superheroes:
1. Technology & Weapons (Avg Probability: 0.42)
2. Combat & Military (Avg Probability: 0.19)
...

## 4. Modifying the Code

To adjust stopword handling, modify preprocess_text().

To change LDA topic names, edit TOPIC_NAMES_AVENGERS and TOPIC_NAMES_HORROR in main.py.

## Notes

The script automatically removes character names (e.g., "tony", "steve", "ganush") from the analysis.

Only Avengers documents are used for the first 5 topics, and only Horror documents for the last 5 topics.
