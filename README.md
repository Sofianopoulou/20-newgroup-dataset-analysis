# Text Mining and Association Rules in Newsgroups

## Overview
This Python program is designed for text mining and discovering association rules within a dataset of newsgroup documents. The dataset used is the "20 Newsgroups" dataset, and the program performs text preprocessing, TF-IDF (Term Frequency-Inverse Document Frequency) analysis, and association rule mining. Additionally, it includes a text classification section where association rules are generated based on the category of the newsgroup.

## Prerequisites
- Ensure that the required Python libraries are installed by running:
  ```bash
  pip install nltk pandas scikit-learn mlxtend
  ```

## Usage (skip if you download the program directly from github)
1. Download the "20 Newsgroups" dataset in tar.gz format from [here](http://qwone.com/~jason/20Newsgroups/).
2. Save the downloaded file as "20news-bydate.tar.gz" in the same directory as the program.
3. Run the provided Python script.

## Program Flow

### 1. Data Extraction
- The script extracts the contents of "20news-bydate.tar.gz" and organizes the newsgroup documents into training and testing sets.

### 2. Preprocessing of Training Set
- Text documents in the training set are preprocessed by removing punctuation, converting to lowercase, tokenizing, removing stop-words, and performing stemming.

### 3. TF-IDF Analysis
- The program utilizes the TF-IDF weighting scheme to analyze the training set, generating a matrix of TF-IDF weights for each term.

### 4. Association Rules (General)
- Association rules are generated based on frequent item-sets using the Apriori algorithm.
- Rules are displayed with support and confidence above specified thresholds.

### 5. Text Classification
- Documents are preprocessed with category information (newsgroup label) added.
- TF-IDF analysis is performed on the new dataset.
- Association rules are generated based on the category of the file being on the right side of the rule.

## Configuration
- You can adjust parameters such as `min_support`, `min_confidence`, and `k` for fine-tuning association rule mining.

## Outputs
- The program outputs association rules for both general terms and terms related to newsgroup categories.

## Important Note
- The script assumes the presence of the "20news-bydate.tar.gz" file and directories "20news-bydate-train" and "20news-bydate-test." Ensure that these directories are present in the same location as the script.

Feel free to explore and modify the script for your specific use case or dataset. Happy mining!
