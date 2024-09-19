# Target E-Commerce Sales Analysis and Product Recommender

## Introduction
This project analyzes the Target e-commerce sales dataset to understand customer behavior and develop a product recommender system. The dataset contains detailed information on 100,000 orders from 2016 to 2018, including data on order status, pricing, payment, shipping, customer demographics, product attributes, and reviews. Our goal is to identify patterns in customer purchases and recommend relevant products based on user preferences.

We leverage the K-Means clustering algorithm to segment customers based on their purchasing behavior and preferences, allowing us to offer personalized product recommendations. By analyzing features such as product categories, order value, payment types, and customer locations, we aim to extract insights that improve customer satisfaction and drive sales.

- Dataset: [Target Dataset on Kaggle](https://www.kaggle.com/datasets/devarajv88/target-dataset)

## K-Means Clustering for Customer Segmentation
The K-Means algorithm is employed to cluster customers into distinct groups based on their behavior. This process involves several steps:

1. **Preprocessing**: 
   - We use a `ColumnTransformer` to handle both numerical and categorical data separately. 
   - **Numerical features** are normalized using `StandardScaler` for consistency in scale.
   - **Categorical features** are transformed into binary vectors using `OneHotEncoder`.

2. **Optimal Clusters**: 
   - After comparing the clustering results for k=2 and k=3, we determined that **k=3** offers the best segmentation performance. These clusters represent different customer segments with unique purchasing behaviors.

## Delivery Time Prediction
In addition to clustering, we built a **Decision Tree Classifier** to predict whether an order would be delivered early, based on various features.

1. **Feature Engineering**:
   - Derived new features like `delivery_time` and `early_delivery` to improve prediction accuracy.
   
2. **Preprocessing**:
   - Similar to the clustering model, we preprocessed the data by normalizing numerical features and encoding categorical variables.

## Conclusion

### Insights and Recommendations:
- **Customer Segmentation**: Clustering reveals valuable insights into customer segments, enabling businesses to tailor marketing strategies and personalized promotions to enhance customer engagement and retention.
  
- **Product Recommendations**: The customer segmentation allows for the development of targeted product recommendations. These can be further refined using real-time data and feedback to ensure relevance and effectiveness.
  
- **Operational Efficiency**: Predicting delivery times can significantly optimize logistics and resource management. This predictive model can help businesses reduce operational costs and improve service quality by accurately forecasting delivery outcomes.

## Summary
This project demonstrates how customer segmentation and delivery time prediction models can provide actionable insights to improve e-commerce operations. By understanding customer preferences, offering personalized product recommendations, and optimizing delivery logistics, businesses can enhance customer satisfaction and gain a competitive edge in the market.
