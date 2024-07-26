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

## Data Descriptions

This dataset includes various economic and housing-related indicators used to analyze the **S&P/Case-Shiller U.S. National Home Price Index** (Target). Below is a brief description of each variable:

- **Target**: **S&P/Case-Shiller U.S. National Home Price Index** - A measure of the value of residential real estate across the United States.

- **all_Const_Emp**: **All Employees, Residential Building Construction** - Total number of employees in the residential building construction sector.

- **emratio**: **Employment-Population Ratio** - The ratio of the employed population to the total population.

- **gdp**: **Gross Domestic Product** - The total market value of all goods and services produced in the United States.

- **home_ow_rate**: **Homeownership Rate (Percentage)** - The percentage of homes occupied by the owners.

- **house_st**: **Housing Starts (New Housing Project)** - The number of new residential construction projects that have begun during a particular period.

- **IPI_Cement**: **Industrial Production: Cement** - A measure of the production output of the cement industry.

- **labor_percent**: **Labor Force Participation Rate** - The percentage of the population that is either employed or actively seeking employment.

- **monthly_supply**: **Monthly Supply of New Houses in the United States** - The number of months it would take to sell the current inventory of new houses at the current sales rate.

- **MSPUS**: **Median Sales Price of Houses Sold for the United States** - The median price at which houses are sold.

- **new_private_house**: **New Privately-Owned Housing Construction Completed (Total units in thousands)** - The total number of new privately-owned housing units completed.

- **new_private_hw_under**: **New Privately-Owned Housing Units Under Construction: Total Units (thousands)** - The total number of new privately-owned housing units currently under construction.

- **p_saving_rate**: **Personal Saving Rate (Percent)** - The percentage of personal income that individuals save rather than spend on consumption.

- **ppi_cement**: **Producer Price Index - Cement Manufacturing** - The average change over time in the selling prices received by domestic producers for their output in the cement manufacturing sector.

- **PPI_Concrete**: **Producer Price Index by Industry: Concrete Brick** - The average change over time in the selling prices received by domestic producers in the concrete brick industry.

- **total_emp_cons**: **All Employees, Construction (Thousands of persons)** - The total number of employees working in the construction sector.
