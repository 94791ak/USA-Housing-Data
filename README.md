# USA HOUSING - Data Science Model

Welcome to the "Exploring US Home Price Trends" project! This project delves into understanding the factors affecting home prices in the United States over the last two decades. Using publicly accessible data and advanced data science methodologies, we aim to create a model that explains how various elements correlate with housing prices.

## Project Breakdown

- **Data Cleaning**: [Process and methods for cleaning and preparing the data.](https://github.com/Npps1997/USA-HOUSING--Data-Science-Model/blob/main/Data_Cleaning_LLC.ipynb)
- **Exploratory Data Analysis (EDA)**: [Exploration of data relationships and patterns.](https://github.com/Npps1997/USA-HOUSING--Data-Science-Model/blob/main/EDA_LLC.ipynb)
- **Model Training**: [Techniques for training and assessing the model.](https://github.com/Npps1997/USA-HOUSING--Data-Science-Model/blob/main/model_training_LLC.ipynb)

## Tools and Libraries Used

- **Programming Language**: Python
- **Data Analysis**: NumPy, pandas
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: scikit-learn
- **Version Control**: Git, GitHub
- **Jupyter Notebooks**: For interactive data exploration

## Data Overview

The project uses a variety of economic indicators and housing market metrics, including:
- S&P/Case-Shiller U.S. National Home Price Index
- Population, Personal Income, GDP, Unemployment Rate, Mortgage Rate
- Housing starts, Homeownership Rate, and more

## Key Features and Correlations

The table below shows the correlation between selected features and the home price index:

| Feature                | Correlation |
|------------------------|-------------|
| MSPUS                  | 0.980       |
| PPI_Cement             | 0.964       |
| GDP                    | 0.961       |
| Income                 | 0.956       |
| PPI_Concrete           | 0.939       |
| Population             | 0.897       |
| Mortgage Rate          | -0.731      |
| Labor Participation    | -0.788      |

## Model Selection and Evaluation

For this analysis, we opted for **Lasso regression** due to its effectiveness in handling multicollinearity. We fine-tuned the model using cross-validation:

- **Best alpha value**: 0.0576
- **Average R-squared score**: 0.9937
- **R-squared score variance**: 0.0009

## Significant Predictors

The following features have significant coefficients, indicating their importance in predicting home prices:

| Feature                | Coefficient  |
|------------------------|--------------|
| Personal Saving Rate   | -0.923       |
| GDP                    | 18.500       |
| MSPUS                  | 26.853       |
| Others                 | ...          |

## Features with Minimal Impact

Some features had negligible coefficients, indicating they are less influential in predicting home prices:

| Feature               | Coefficient  |
|-----------------------|--------------|
| Mortgage Rate         | 0.0          |
| PPI_Cement            | 0.0          |
| Permit                | 0.0          |
| Others                | ...          |

## Data Sources

The data used in this project was obtained from the Federal Reserve Economic Data (FRED) at https://fred.stlouisfed.org/.
