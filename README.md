Customer Segmentation with Unsupervised Learning

## Overview

This project uses **unsupervised learning** techniques, specifically **K-means clustering**, to segment customers into different groups based on their order behaviors and monetary value. The dataset provided contains information about 20,000 customers, including their order history, value spent both online and offline, and their preferred categories.

The goal of the project is to:

- Perform **Exploratory Data Analysis (EDA)** to understand the dataset.
- Apply **K-means clustering** to group customers into segments.
- Visualize the segments using **PCA (Principal Component Analysis)**.
- Evaluate the results using the **Silhouette Score** to select the optimal number of clusters.
- Save the trained models for future use in predictions.

## Dataset

The dataset used for customer segmentation is a CSV file named `flo_data_20k.csv`. The dataset includes the following columns:

- `master_id`: Unique identifier for each customer.
- `order_channel`: The channel through which the customer made the order.
- `last_order_channel`: The channel used for the customer's most recent order.
- `first_order_date`: The date when the customer first placed an order.
- `last_order_date`: The date of the customer's most recent order.
- `last_order_date_online`: The date of the most recent online order.
- `last_order_date_offline`: The date of the most recent offline order.
- `order_num_total_ever_online`: Total number of orders placed online.
- `order_num_total_ever_offline`: Total number of orders placed offline.
- `customer_value_total_ever_offline`: Total monetary value spent offline.
- `customer_value_total_ever_online`: Total monetary value spent online.
- `interested_in_categories_12`: Categories the customer is interested in (12 total categories).

## Requirements

To run this project, you will need to install the following Python packages:

```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
scipy
```

You can install them using `pip`:


## Model Saving and Predictions

After training the K-means clustering model, the model, scaler, and label encoders are saved using `joblib` for later use. The saved models can be loaded to make predictions on new customer data. Here's an example:

## Evaluation and Results

- **Silhouette Score** was used to evaluate the clustering quality, and the optimal number of clusters was found to be **6**, based on the highest Silhouette score of **0.3556**.
- The customer segments were visualized using **PCA** to reduce the dimensionality of the dataset and plot the clusters in a 2D space.

## Insights

From the customer segmentation process, the following insights were gained:

- Different segments of customers (e.g., high-value, low-frequency, etc.) can be targeted with tailored marketing strategies.
- The **recency**, **frequency**, and **monetary** values (RFM model) play a crucial role in differentiating customers.
- The clusters can help businesses optimize their marketing campaigns by identifying the most valuable customers and engaging with less active ones.
