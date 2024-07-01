# Steam Games Analysis

## Overview
This project involves cleaning, processing, and analyzing a dataset of Steam games to gain insights and build predictive models. The dataset is sourced from a CSV file named `SteamScrappedData.csv`. The analysis includes data cleaning, feature engineering, visualization, and machine learning model training.
## Data Cleaning
The data cleaning process involves:

- Dropping unnecessary columns (`url`, `types`, `desc_snippet`, `all_reviews`, `game_details`, `publisher`, `popular_tags`, `languages`, `game_description`, `mature_content`, `minimum_requirements`, `recommended_requirements`, `discount_price`).
- Handling missing values:
  - Filling missing `original_price` values with `discount_price`.
  - Dropping rows with missing `recent_reviews`, `developer`, and `genre`.
  - Filling missing `achievements` with `0`.
- Converting `original_price` to numeric and handling 'Free to Play' games.
- Converting `release_date` to a standard date format and handling missing values.

## Feature Engineering
Feature engineering includes:

- Encoding review sentiments (`Very Positive`, `Mixed`, etc.) to numerical values.
- Calculating the number of achievements, genres, and age of the game.
- Determining if a game is free-to-play.
- Calculating developer popularity and whether a game is multiplayer.
- Calculating average reviews by genre.
- Identifying trending games based on various features.

## Visualizations
Several visualizations are created using seaborn and plotly:

- Distribution of average reviews by genre.
- Distribution of achievements for top 10 games in trending genres.
- Bar chart of trending games across genres.
- Top 5 games in trending genres with positive sentiment.
- Sentiment distribution histogram.

## Machine Learning Models
Multiple machine learning models are trained and evaluated:

- **Logistic Regression**: For predicting trending games.
- **Support Vector Machine (SVM)**: For predicting trending games.
- **Artificial Neural Network (ANN)**: For predicting trending games.
- **Long Short-Term Memory (LSTM) Neural Network**: For predicting trending games.
- **ANN for Positive Reviews**: For predicting positive reviews based on several features.

## Results
Results from model evaluations:

- **Logistic Regression**: Achieved an accuracy score.
- **SVM**: Achieved an accuracy score.
- **ANN**: Achieved an accuracy score for predicting trending games and positive reviews.
- **LSTM**: Achieved an accuracy score.

## Installation
To run this project, you'll need Python and the following libraries installed:

- numpy
- pandas
- seaborn
- matplotlib
- scikit-learn
- tensorflow
- plotly

You can install these libraries using pip:

```bash
pip install numpy pandas seaborn matplotlib scikit-learn tensorflow plotly
