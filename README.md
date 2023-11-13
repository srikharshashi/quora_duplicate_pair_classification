# Duplicate Question Pair (Quora) Classification Using NLP

## Overview

This project was developed for a Kaggle competition hosted by Quora. The objective is to determine if two questions have the same semantic meaning, with the goal of grouping similar questions together. The competition involved extensive feature engineering, requiring the creation of 21 custom features from the provided dataset.

## Dataset Overview

The dataset for this project was provided by Quora for the competition. It consists of three columns:

| question1 (str) | question2 (str) | isDuplicate (t/f) |
|-----------------|-----------------|-------------------|
| ...             | ...             | ...               |

[Link to Dataset](https://www.kaggle.com/competitions/quora-question-pairs/data)


## Pre-Processing 

- Replacing special characters
- Removing some characters which arent' in unicode
- Reducing numbers to actual string names
- Removing shortforms and replace with long forms
- Removing HTML tags

## Custom Features Overview

### Advanced Features

#### Token Features

- cwc_min: This is the ratio of the number of common words to the length of the smaller question
- cwc_max: This is the ratio of the number of common words to the length of the larger question
- csc_min: This is the ratio of the number of common stop words to the smaller stop word count among the two questions
- csc_max: This is the ratio of the number of common stop words to the larger stop word count among the two questions
- ctc_min: This is the ratio of the number of common tokens to the smaller token count among the two questions
- ctc_max: This is the ratio of the number of common tokens to the larger token count among the two questions
- last_word_eq: 1 if the last word in the two questions is same, 0 otherwise
- first_word_eq: 1 if the first word in the two questions is same, 0 otherwise
- Total *8*

#### Length Based Features

- mean_len: Mean of the length of the two questions (number of words)
- abs_len_diff: Absolute difference between the length of the two questions (number of words)
- longest_substr_ratio: Ratio of the length of the longest substring among the two questions to the length of the smaller question
- Total *3*

#### Fuzzy Features

- fuzz_ratio: fuzz_ratio score from fuzzywuzzy
- fuzz_partial_ratio: fuzz_partial_ratio from fuzzywuzzy
- token_sort_ratio: token_sort_ratio from fuzzywuzzy
- token_set_ratio: token_set_ratio from fuzzywuzzy 
- Total *4*

### Basic Features

- length of questions
- total of words
- count of common words
- ratio - word share



## How to Run

Follow these steps to run the project locally:

0. Clone the repository:
   ```bash
   git clone https://github.com/srikharshashi/<reponame>
   cd <reponame>
   ```

1.Install dependencies:

    pip install -r requirements.txt

2. Run with streamlit:

    ` streamlit run infer.py `


## Screenshots
[Leave empty for future insertion of images]

## Accuracy

The project achieved the following accuracies on the test set:

| Model          | Accuracy       |
|----------------|----------------|
| Random Forest  | 78.79%         |
| XGBoost        | 80.1%          |



