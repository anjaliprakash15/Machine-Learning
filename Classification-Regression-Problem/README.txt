README

## Overview
This project implements a machine learning system to predict if a player will last over 5 years or not.

## The Data
The dataset is NBA Rookie Stats from data.world. This dataset totals 21 columns and 1340 rows. The 21 features are play name (Name), games played (GP), minutes played (MIN), points per game (PPG), field goals made (FGM), field goal attempts (FGA), field goal percent (FG%), three points made (3PM), three point attempts (3PA), three point percent (3P%), free throws made (FTM), free throw attempts(FTA), free throw percent (FT%), offensive rebounds (OREB), defensive rebounds (DREB), rebounds (REB), assists (AST), steals (STL), blocks (BLK), turnovers (TOV), and target(TAR). Each row in the table represents a player’s rookie statistics, stats of that player’s first season.
Out of these 21 attributes, the last attribute is the class attribute for which the system
will predict about. It is a Boolean attribute, where “o” means the career length of the player is less than 5 years, and “1” greater than or equal to 5 years. 

## Data Preparation
The 'Name' column was removed.
The 'TAR' column was converted into integer format.
Missing values were imputed with mean values.

## Feature Normalization
Features were normalized using StandardScaler to improve performance for distance-based models.

## Regularization in Logistic Regression
Penalty = None- F1 Score: 0.8011
Penalty = L1- F1 Score: 0.8011
Penalty = L2- F1 Score: 0.8056
Penalty = ElasticNet- F1 Score: 0.8011
The best performing penalty was L2 regularization, keeping overfitting and performance balanced.

## Hyperparameter Tuning
GridSearchCV was used to fine tune model hyperparameters.
Random Forest: Optimal 'n_estimatores=200' (CV F1 Score:0.7413 )
Logistic Regression: Optimal penalty = 'L2' (Test F1 Score:0.8056 )

## Model Performance
F1 Scores of models on test set:
KNN- 0.7598
Random Forest- 0.7765
Logistic Regression (L2 penalty)- 0.8056 (Best)
ANN- 0.7811
Best performing model was Logistic Regression with L2 regularization.

## TO RUN THE MODEL
1. Dependencies should be installed.
	pip install pandas numpy matplotlib scikit-learn
2. Run the model
	python project2.py




Author: Anjali Prakash






