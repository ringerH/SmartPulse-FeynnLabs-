## SmartPulse - Customer Analytics dashboard prototype for small businesses
Covers EDA, Data Visualization and ML Modelling for the prototype product.

[Kaggle Notebook](https://www.kaggle.com/code/hillol10/customer-segmentation-kmeans)

## Overview

SmartPulse is a product designed to offer actionable customer insights for small businesses. This document summarizes the exploratory data analysis (EDA) and machine learning (ML) modelling processes used to understand customer spending behavior and identify valuable customer segments.

## Exploratory Data Analysis (EDA)

### Initial Analysis

- **Data Overview**: The dataset includes the following attributes:
  - `CustomerID`
  - `Gender`
  - `Age`
  - `Annual Income ($)`
  - `Spending Score (1-100)`
  - `Profession`
  - `Work Experience`
  - `Family Size`
- **Missing Values**: Missing values were found in the `Profession` attribute and were handled through imputation or feature engineering.

### Feature Engineering

- **New Features Created**:
  - `Family_Income_Product`: Product of `Family Size` and `Annual Income ($)`.
  - `Family_Income_Ratio`: Ratio of `Family Size` to `Annual Income ($)`.
- **Encoding**:
  - `Gender` was one-hot encoded to binary values.
  - `Profession` was label encoded into numerical values.
- **Scaling**: Numerical features, including newly created features, were scaled to have zero mean and unit variance.

### Visualization

- **Scatter Plots**: Examined relationships between `Spending Score` and other features:
  - `Gender`: Insights into spending score differences between genders.
  - `Family Size`: Patterns indicating how family size affects spending scores.
  - `Work Experience`: Correlation between work experience and spending score.
  - `Annual Income`: Impact of income on spending behavior.

### Insights

- **High Spending Score Patterns**: Identified that individuals with:
  - Annual income > $50,000
  - Family size < 8
  - Work experience <= 10 years
  Tend to have higher spending scores.

## Machine Learning Modelling

### Feature Preparation

- **Data Encoding and Scaling**: Categorical variables were encoded, and numerical features were scaled to prepare for modeling.
- **New Features Integration**: Incorporated engineered features such as `Family_Income_Product` and `Family_Income_Ratio` into the model.

### Clustering Model

- **Model Used**: KMeans clustering was applied to group customers based on their spending behavior and other attributes.
- **Performance Evaluation**:
  - **Silhouette Score**: Assessed the quality of the clusters, indicating how well-separated and defined the clusters are.

### Results

- **Cluster Identification**: KMeans model identified distinct clusters of customers based on their spending scores and associated features.
- **Insight Generation**: Clustering results are used to:
  - Tailor marketing strategies
  - Identify high-value customer segments
  - Enhance customer engagement for SmartPulse

## Conclusion

The EDA and ML modelling processes for SmartPulse have effectively:

- **Identified Key Features**: Pinpointed critical attributes influencing spending scores.
- **Enhanced Feature Set**: Improved model performance by creating and integrating new features.
- **Segmented Customers**: Provided valuable insights into customer segments, enabling targeted strategies and better decision-making.

These steps have laid the foundation for leveraging SmartPulse to offer actionable insights and recommendations to small businesses, enhancing their understanding of customer behavior and optimizing their marketing efforts.

## Next Steps

1. **Deploy the Model**: Use the trained model for live analytics and customer segmentation.
2. **Implement Dashboard**: Develop and deploy an interactive dashboard for real-time insights.
3. **Continued Improvement**: Refine features and models based on ongoing feedback and additional data.

For further details and code, please refer to the repository files.

