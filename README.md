# Exploratory Data Analysis (EDA) of Orders Data

## Project Objective

The primary objective of this project, as outlined in `TASK 5 DA.pdf`, is to extract meaningful insights from the provided `Orders.csv` dataset using visual and statistical exploration techniques. This analysis aims to uncover patterns, trends, and anomalies that can inform business decisions.

## Dataset Overview

The `Orders.csv` dataset contains 500 entries across 5 columns, providing transactional details.

-   **Order ID**: Unique identifier for each order.
-   **Order Date**: The date when the order was placed.
-   **CustomerName**: Name of the customer who placed the order.
-   **State**: The state from which the order originated.
-   **City**: The city from which the order originated.

Initially, all columns were interpreted as `object` (string) type by Pandas. No missing values were found in the raw dataset.

## Data Cleaning & Preparation

Before proceeding with the analysis, the following data cleaning and preparation steps were performed:

1.  **Date Conversion**: The 'Order Date' column was converted from `object` (string) to a `datetime` format.
    -   **Why**: To enable time-based aggregation and trend analysis (e.g., orders per year, month).
2.  **Temporal Feature Extraction**: New columns were derived from the 'Order Date' to facilitate detailed temporal analysis:
    -   `Order Year`: Extracts the year of the order.
    -   `Order Month`: Extracts the numerical month (1-12).
    -   `Order Month Name`: Extracts the full name of the month (e.g., 'January').
    -   `Order Day`: Extracts the day of the month.
    -   `Order Day of Week`: Extracts the full name of the day of the week (e.g., 'Monday').
    -   **Why**: These features allow for analyzing annual trends, monthly seasonality, and daily order patterns.
3.  **Duplicate Check**: The dataset was checked for duplicate rows based on all columns.
    -   **Why**: Duplicate records can skew analysis results by artificially inflating counts or averages. In this case, no duplicate rows were found.

## Questions Explored via EDA

**1. What are the overall order trends over time (yearly, monthly)?**

**2. Which states contribute the most to the total orders?**

**3. Which cities are the top performers in terms of order volume?**

**4. Who are the most active customers (highest number of orders)?**

**5. Is there any seasonality in the orders (e.g., specific months or days of the week with higher activity)?**

**6. How do order volumes vary across cities within top states?**

## Exploratory Data Analysis (EDA) & Visualizations
The analysis utilizes value_counts() for frequency distributions and various plots from matplotlib.pyplot and seaborn for visualization.

**1. Orders Over Time (Yearly Trend)**
Description: This line plot visualizes the total number of orders placed each year.

Insight: This helps in understanding the long-term growth or decline in order volumes. For this dataset, orders are primarily concentrated in 2018.
