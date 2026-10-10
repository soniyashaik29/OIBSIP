# Retail Sales Data Analysis using Python

## Project Overview

This project focuses on performing **Exploratory Data Analysis (EDA)** on a retail sales dataset using Python. The goal is to understand sales performance, customer segments, product performance, regional trends, and shipping efficiency through data analysis and visualizations.

The analysis helps identify business insights that can support better decision-making in sales, inventory management, and customer service.

## Objectives

- Understand the structure and characteristics of the retail sales dataset.
- Clean and prepare the data for analysis.
- Identify and handle missing values.
- Analyze customer segments and customer distribution.
- Identify the top-performing products based on sales revenue.
- Compare sales performance across product categories and regions.
- Examine the relationship between sales and shipping duration.
- Visualize key patterns and trends.
- Provide actionable business recommendations.

## Dataset Description

The dataset used in this project is a retail Superstore sales dataset.

It contains information about orders, customers, products, sales, and shipping.

**Key columns include:**

| Column       | Description                             |
| ------------ | --------------------------------------- |
| Order ID     | Unique identifier for an order          |
| Order Date   | Date when the order was placed          |
| Ship Date    | Date when the order was shipped         |
| Ship Mode    | Shipping method used                    |
| Customer ID  | Unique identifier for a customer        |
| Segment      | Customer segment                        |
| Region       | Geographic sales region                 |
| Category     | Product category                        |
| Sub-Category | Product sub-category                    |
| Product Name | Name of the product                     |
| Sales        | Revenue generated from sales            |
| Postal Code  | Customer's postal code, where available |

_Note: The analysis is based on the columns available in the dataset. Variables such as age, gender, quantity, profit, and discount are not included in the version used for this project._

## Tools and Technologies

- **Python** – Main programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualizations
- **Jupyter Notebook** – Interactive analysis environment

## Project Workflow

### 1. Data Loading

Load the retail sales dataset into a Pandas DataFrame.

### 2. Data Inspection

Examine the dataset's dimensions, column names, data types, and sample records.

### 3. Data Cleaning

- Check for missing values.
- Identify duplicate records.
- Convert date columns to datetime format.
- Verify and correct data types where necessary.

### 4. Customer Segment Analysis

Analyze the distribution of customers across different segments and compare the number of unique customers in each segment.

### 5. Product Performance Analysis

Identify the top 10 products based on total sales revenue.

### 6. Category-Wise Sales Analysis

Compare total sales across product categories to identify the categories contributing the most revenue.

### 7. Correlation Analysis

Examine the relationship between sales and shipping duration using a correlation heatmap.

### 8. Shipping Analysis

Calculate shipping duration from order and ship dates and compare average delivery-processing time across shipping modes.

### 9. Regional Sales Analysis

Compare sales across regions to identify strong-performing markets and potential growth opportunities.

### 10. Business Insights

Summarize the main findings and provide recommendations based on the analysis.

## Installation and Setup

Make sure Python is installed on your system.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## How to Run the Project

1. Download or clone this repository.
2. Extract the dataset archive if the data is provided as a ZIP file.
3. Place the dataset CSV file in the project directory or update the file path in the notebook.
4. Open a terminal in the project directory.
5. Start Jupyter Notebook:

```bash
jupyter notebook
```

6. Open the project notebook and run the cells in order, starting with data loading and continuing through the analysis and visualizations.

## Expected Outputs

The project generates:

- Dataset overview and summary statistics
- Missing-value and duplicate checks
- Customer segment distribution charts
- Top 10 products by sales revenue
- Category-wise sales visualizations
- Correlation heatmap
- Average shipping duration by shipping mode
- Regional sales comparison
- Business insights and recommendations
- Cleaned dataset and exported summary files

## Business Recommendations

Based on the results of the analysis, businesses can:

- **Improve inventory planning:** Prioritize products and categories with higher sales.
- **Optimize marketing strategies:** Tailor campaigns to customer segments based on their purchasing patterns.
- **Improve shipping efficiency:** Review shipping methods associated with longer shipping durations.
- **Strengthen regional performance:** Identify regions with lower sales and investigate opportunities for growth.
- **Monitor sales trends:** Regularly track category, product, and regional performance to support business decisions.

These are potential recommendations; the final priorities should be based on the actual results produced by the analysis.

## Limitations

- The dataset does not contain age or gender information, so demographic analysis cannot be performed.
- Quantity, profit, and discount fields are unavailable in this dataset version, limiting unit-volume and profitability analysis.
- Shipping duration is calculated using the difference between ship date and order date. It measures the time until shipment, not necessarily the actual time until customer delivery.
- Correlation does not establish causation.

## Conclusion

This project demonstrates how Python can be used to explore retail sales data, identify patterns, and communicate findings through visualizations. The analysis provides a foundation for understanding customer segments, product performance, category-wise sales, regional trends, and shipping efficiency.

The insights can help guide data-driven decisions and highlight areas for further investigation.
