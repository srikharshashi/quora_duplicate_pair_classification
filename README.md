# Duplicate Question Pair (Quora) Classification Using NLP

## Overview

This project was developed for a Kaggle competition hosted by Quora. The objective is to determine if two questions have the same semantic meaning, with the goal of grouping similar questions together. The competition involved extensive feature engineering, requiring the creation of 21 custom features from the provided dataset.

## Dataset Overview

The dataset for this project was provided by Quora for the competition. It consists of three columns:

| question1 (str) | question2 (str) | isDuplicate (t/f) |
|-----------------|-----------------|-------------------|
| ...             | ...             | ...               |

[Link to Dataset](insert_link_here)

## Custom Features Overview

[To be inserted later]

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



