# Behavioral Shopper Classification and Product Interaction Prediction

This project explores how machine learning can be used to classify online shoppers based on behavioral data and predict their next likely interaction level with product categories. By combining psychological profiling with browsing metrics, the model provides a foundation for personalized recommendation systems in e-commerce environments.

## Objective

1. **Shopper Classification**: Identify whether a user is an impulse buyer, bargain hunter, or planned spender based on their browsing behavior.
2. **Product Interaction Prediction**: Predict the level of engagement (Low, Medium, or High) a user will have with product pages in their current or next session.

## Dataset

- **Source**: [UCI Online Shoppers Purchasing Intention Dataset on Kaggle](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store)
- **Rows**: 12,330
- **Features**: 18
- **Description**: The dataset contains session-level information including page views, bounce rates, time spent, and other behavioral metrics.

## Methodology

### 1. Data Preprocessing
- Handled categorical variables: `Month`, `VisitorType`, `Weekend`
- Standardized numerical features
- Ensured no missing values

### 2. Clustering Users with K-Means
- Used features such as time spent, bounce rates, and review reading to group users into 3 clusters
- Interpreted the clusters as:
  - Cluster 0: Bargain Hunters
  - Cluster 1: Planned Spenders
  - Cluster 2: Impulse Buyers

### 3. Predicting Product Interaction with Random Forest
- Target: Product interaction level (`Low`, `Medium`, `High`) derived from `ProductRelated` feature
- Train-test split: 80/20 with stratification
- Random Forest classifier used for prediction
- Achieved 83% overall accuracy

## Key Results

- **Classification Accuracy**: 83%
- **Strong Performance** on "Medium" and "Low" interaction categories
- **Top Features**: Product duration, exit rates, page values

## Visualizations

- Shopper type distribution (pie chart)
- Top 10 most important features (bar plot)

## Tools and Libraries

- Python 3.x
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook



