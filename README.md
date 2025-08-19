# Nepali Laptop Price Prediction - Web Scraping

Web-scraped Nepali laptop data for price prediction using Python and Machine Learning. This project predicts laptop prices in Nepal based on features extracted from product titles and specifications.



## Project Overview

The goal of this project is to predict laptop prices in Nepal using machine learning. Laptop specifications were scraped from **Infotechs**, and features such as processor, RAM, storage, display, and graphics were extracted to train regression models.

## Project Steps

### 1. Data Loading
- Loaded laptop data from CSV files into pandas DataFrames.

### 2. Data Exploration and Cleaning
- Inspected data structure, missing values, and types.
- Dropped irrelevant columns and renamed for consistency.
- Merged datasets into a single DataFrame.

### 3. Feature Engineering
- Extracted features like `processor`, `ram`, `storage`, `graphics`, `display`, `screensize`, `company`, `processor_feature`, and `processor_brand`.
- Categorized display and graphics types for better model understanding.

### 4. Data Preprocessing
- Handled missing values with `SimpleImputer`.
- Scaled numerical features using `StandardScaler`.
- Encoded categorical features using `OneHotEncoder`.

### 5. Model Selection and Training
- Trained and compared the following models:
  - Linear Regression
  - Random Forest Regressor
  - XGBoost Regressor

### 6. Model Evaluation

Models were evaluated using **R² Score** and **Mean Absolute Error (MAE)**:

| Model                   | R² Score | MAE (in NPR) |
|-------------------------|----------|---------------|
| Linear Regression       | 0.7687   | 11,354        |
| Random Forest Regressor | 0.8866   | 8,075         |
| XGBoost Regressor       | 0.8409   | 8,587         |

**Observation:** Random Forest performed the best in terms of both R² and MAE.

## Code Structure
The notebook contains:
- Data loading and exploration
- Data cleaning and merging
- Feature engineering
- Preprocessing for machine learning
- Training and evaluating models

## Dependencies
Python libraries used:

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- xgboost

Install dependencies with:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
