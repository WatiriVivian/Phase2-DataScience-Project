

## House Price Prediction Analysis for Real Estate Agents In King County
A well executed sample project, that uses multi linear regression and python code to show how to predict house prices based on various factors

# Project overview

This is a sample  project that focuses on analyzing the King County House Sales dataset  to provide accurate predictions of house prices. The analysis aims to assist real estate agents in making informed decisions and providing expert advice to their clients in the King County area.

The objective of this project is to develop a model that accurately predicts house prices based on various features, such as the number of bedrooms, condition, grade,location etc

# Business Problem

The real estate market is a dynamic and complex sector influenced by various economic, demographic, and societal factors. The challenge at hand is to develop a solution that accurately predicts house prices in King County. By leveraging the relationships between different features of a house and its sale price, the goal is to provide real estate agents with the tools they need to make informed decisions.

Accurate price predictions are essential for real estate agents to assess whether a property is appropriately priced and to determine a competitive price. With reliable predictions, agents can confidently advise their clients, helping them make strategic choices regarding buying, selling, or investing in properties. The outcome of this project directly supports real estate agents in offering expert guidance and ensuring optimal outcomes for their clients.

By applying multi linear regression  and analyzing the King County housing dataset, we aim to uncover the significant factors that drive house prices. This analysis will enable real estate agents to navigate the intricacies of the local market and provide accurate pricing recommendations. Ultimately, the project seeks to empower real estate agents with the insights necessary to excel in their profession, optimize their decision-making processes, and deliver exceptional value to their clients.

# Dataset & Data Understanding

This project utilizes the King County House Sales dataset, which is available in the `kc_house_data.csv` file located in the `data` folder of this GitHub repository. A comprehensive description of the column names can be found in the `column_names.md` file in the same folder. While the column names provide some information, it is important to note that further research or informed judgment may be necessary to fully understand the meaning of the data.

The analysis performed on the dataset included the following steps:

1. Data Cleaning: Rows with missing data were dropped, and duplicate entries were removed based on the `id` column.

2. Data Transformation: Categorical data in the `view` and `waterfront` columns were converted into numerical data.

3. Exploratory Data Analysis: Various checks were conducted to assess the linearity assumptions between the target and predictor variables and identify any potential multicollinearity issues.

4. Feature Engineering: Certain columns were transformed to enhance their usefulness. For example, the `date` column was converted into a categorical variable representing the season, and the `yr_renovated` column was modified to indicate the number of years since the last renovation. Additionally, the `yr_built` column was modified to the age of each house.

By performing these steps, we aimed to gain a comprehensive understanding of the dataset and prepare it for further analysis and modeling.


# Methology

The analysis utilizes multiple linear regression, a powerful statistical technique, to identify the significant factors that contribute to house prices in the King County area. By examining the relationships between the independent variables (house features) and the dependent variable (sale price), the model generates predictions that can be used to guide pricing strategies and inform buying or selling decisions.

## Modelling

During the analysis, we developed and evaluated four models to gain insights and make predictions. Here is an overview of the models:

**Model 1: Baseline Model**

The baseline model included nearly all available feature variables. Categorical variables were converted into dummy variables for modeling purposes. We further refined the model by testing for linear assumptions, ensuring that the relationships between the predictors and the target variable followed a linear pattern.

**Model 2: Feature Selection and Refinement**

In the second model, we focused on addressing multicollinearity issues and high p-values associated with certain features. We identified and removed features with high multicollinearity to enhance the model's stability and interpretability. Additionally, we examined linearity assumptions by using partial regression plots and checked for outliers in both the target and predictor variables, subsequently removing any outliers identified.

**Model 3: Assumption Testing and Transformation**

For the third model, we conducted tests to verify key assumptions of linear regression. We assessed homoscedasticity using the Breusch-Pagan test, checked for normality through the Jarque-Bera test and the K-test, and examined the skewness of the target variable. To address skewness, we applied a logarithmic transformation to the target variable, aiming to reduce skewness and improve the model's performance.

By building and refining these models, we aimed to explore different aspects of the data and address potential challenges such as multicollinearity, linearity assumptions, and outliers. The iterative modeling process allowed us to gain insights into the relationships between variables and identify the most appropriate approach for predicting house prices in the King County dataset.

Model 4: Log Transformation 

In this regression model, a log transformation was applied to the dependent variable, which is the housing price (log(price)). The purpose of this transformation was to address potential issues of heteroscedasticity or nonlinearity in the relationship between the predictors and the price.

Model 5: Log transformation of feature variables

In this regression model, a log transformation was applied to the predictor variable 'sqft_living' (square footage of living space). The purpose of this transformation was to address potential nonlinearity in the relationship between the predictor and the housing price.

By taking the logarithm of the 'sqft_living' variable, the model captured the proportional change in the housing price associated with an increase in  the living space. This can be beneficial when the relationship between the predictor and the price is not strictly linear, as it allows for a more flexible and accurate representation of the data.

Model 6: More Log transformation

This regression model aims to explain the relationship between housing prices and various factors. The model uses several predictor variables, such as the number of bedrooms, the size of the living area, the number of floors, the distance from downtown Seattle, the age of the house, whether it has a waterfront view, and the season of sale. Additionally, it includes logarithm transformations of the living area and the age of the house to capture potential nonlinear relationships.
Model 6 was the model of choice for the analysis. It provided most  insights into the factors influencing housing prices


# Regression Results
Some of the significant results of the regression analysis were:
Spring and summer are the best times to sell houses while fall and winter are the best times to buy

Square Footage of Living Space: The square footage of living space has a positive impact on house prices. As the size of the living space increases, the estimated price of the house also increases. This indicates that larger houses are generally priced higher.

Floors: The number of floors in a house positively affects house prices. Houses with more floors tend to have higher estimated prices. This suggests that multi-story houses are generally valued more than single-story houses.

As the age of the house increases, the estimated price also increases. This could be due to factors such as historical significance or architectural value associated with older houses.

Houses located on the waterfront have significantly higher estimated prices compared to houses that are not on the waterfront. Waterfront properties are considered desirable and tend to command higher prices due to the scenic views and potential for recreational activities.

The Analysis has more insights on the other factors.

# Conclusion

The House Price Prediction Analysis offers real estate agents in King County a valuable tool for accurate price estimations and informed decision making. By leveraging multiple linear regression, the project provides insights into the factors influencing house prices and enables agents to optimize their strategies, offer expert advice, and stay ahead in a competitive real estate market.

Real estate agents can utilize the predictions and market insights to guide their clients, build trust, and drive successful transactions. By incorporating data-driven approaches into their practices, agents can enhance their reputation as reliable professionals and provide an exceptional level of service to homebuyers and sellers in the King County area.

# Installations

This project requires Python 3.11 and the following Python libraries installed:

Numpy

Pandas

matplotlib

scikit-learn

scipy

Seaborn

statsmodels

we also reccommend to install Anaconda, a pre-packaged Python distribution that contains all of the necessary libraries and software for this project which also include jupyter notebook to run and execute IPython Notebook.

# Contributing Instructions

As an open-source project, we highly value transparency and welcome contributions from the community. We appreciate your support in various ways, including bug fixes, feature proposals, documentation improvements, and spreading the word about our project. 

Bug Report: If you encounter any error messages or come across issues while using our code, we kindly request you to create a bug report. This will help us identify and address the problems effectively.

Feature Request: If you have any innovative ideas or find yourself in need of additional functionalities that would enhance the development process and improve the robustness of our project, we encourage you to submit a feature request. Your input is valuable in shaping of the project.

Documentation Request: If you find any gaps or areas where the King County HOuse price analysis documentation can be improved, please submit a documentation request. Your feedback will assist us in providing comprehensive and helpful resources for all users.


