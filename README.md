# CS:GO Round Winner Prediction using Machine Learning

This project aims to predict the winner of a CS:GO round (Counter-Terrorists or Terrorists) using machine learning techniques. The model is trained on structured in-game data to perform binary classification based on various round-specific features such as player health, armor, money, weapon value, grenade value, and map-related data.

## Project Overview

- **Problem Statement**: Predict which team (CT or T) will win a CS:GO round.
- **Dataset**: `csgo_round_snapshots.csv` containing ~122,000+ rows and 97 columns.
- **Target Variable**: `round_winner` (values: CT or T).
- **Features**: Include map, round time remaining, bomb planted status, health, armor, money, players alive, weapon and grenade values for both teams.
- **Approach**:
  - Data Cleaning: Removed duplicates and checked for missing values.
  - Encoding: Categorical features like `map`, `bomb_planted`, and `round_winner` encoded using Label Encoding.
  - Feature Selection: All relevant features retained except the target variable.
  - Train-Test Split: 80% training, 20% testing with a fixed random state for reproducibility.
  - Model Used: Logistic Regression (initial baseline model).
  - Evaluation Metrics: Accuracy, Confusion Matrix, Classification Report.

## Model Training & Evaluation

The logistic regression model was trained using Scikit-learn:




Baseline Accuracy: ~86% (depending on preprocessing and encoding)

Insights: The model performs well due to strong game mechanics and clear feature signals like health, weapon value, and bomb status.


Technologies Used
Python

Pandas, NumPy

Scikit-learn

Jupyter Notebook / Google Colab
