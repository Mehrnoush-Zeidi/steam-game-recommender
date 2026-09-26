# Steam Game Recommender System

## Overview

This project develops a recommender system for Steam games using user behavioural data, with a focus on purchases and game play duration.

The recommendation system uses **Collaborative Filtering with the Alternating Least Squares (ALS)** algorithm to generate personalised game recommendations.

The project follows these main stages:

1. Data Pre-processing
2. Exploratory Data Analysis (EDA)
3. Model Training
4. Model Evaluation
5. Hyperparameter Tuning
6. Recommender Generation

## Dataset

The dataset used in this project is not included in this repository due to restrictions on public distribution.

## Methodology

The original Steam behavioural data contains information about users, games, behaviours, and interaction values.

The behavioural data is processed to construct an implicit rating based on game play hours. The project applies a logarithmic transformation:

```python
rating = log1p(hours)
```

This transformed value is used as the rating signal for the recommendation model.

The project creates integer IDs for games so that they can be used with the ALS matrix-factorisation approach.

The ALS model is trained using user-game interactions and evaluated using RMSE. The project also explores different model configurations through hyperparameter tuning.

Finally, the trained model is used to generate the top game recommendations for users.

## Technologies

- Python
- PySpark
- Apache Spark MLlib
- MLflow
- Databricks
- ALS Collaborative Filtering

## Experiment Tracking

The project uses **MLflow** for experiment tracking in the original Databricks environment.

The workflow includes multiple model configurations and records model evaluation information, including RMSE, during hyperparameter tuning.

## Project Structure

```text
steam-game-recommender/
│
├── steam_game_recommender.ipynb
├── README.md
└── requirements.txt
```

## Dataset

The dataset used in this project is not included in this repository due to restrictions on public distribution.

## Environment

The original project was developed using a Databricks environment with Apache Spark and MLflow.

Some parts of the notebook, including dataset access, Databricks utilities, MLflow tracking, and Databricks display functionality, depend on the original Databricks environment.

## Results

The project evaluates the recommender system using RMSE and performs hyperparameter tuning before generating recommendations.

The notebook also produces personalised recommendations for users using the trained ALS model.

## Note

This repository contains the project code and documentation. The dataset is not included due to restrictions on public distribution.
