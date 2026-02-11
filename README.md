# Oviya_Waitrose_Data_Visualisation_Project
Data cleaning and comparative analysis of a bakery dataset using data visualization techniques in Python.

**Bakery Price Analysis Project Report**
Project Report: Comparative Price Analysis of Waitrose Bakery Products
1. Introduction

This project focuses on cleaning, processing, and analyzing a retail bakery dataset sourced from the Waitrose product files. The primary objective is to understand pricing patterns across product categories, with a special emphasis on Everyday Value vs Branded products. The project demonstrates the application of data cleaning techniques, exploratory data analysis (EDA), and comparative visualization to derive meaningful business insights.

The analysis was carried out using Python, with libraries such as Pandas, NumPy, Lets-Plot (ggplot-style visualizations), and supporting utilities for formatting and inspection.

2. Data Description and Ingestion
2.1 Data Source

Multiple CSV files located in the ME204/data/waitrose directory.

Each file represents product-level information including:

Product name

Category

Size

Price (as text)

Branding indicators (Everyday Value / Branded)

2.2 Data Loading Process

The project begins by programmatically listing all files in the directory.

Each file is read into a Pandas DataFrame.

All DataFrames are concatenated into a single unified DataFrame using pd.concat().

Why this approach?

Ensures scalability when working with multiple files.

Maintains consistency across the dataset.

Avoids manual file handling errors.

3. Data Cleaning and Preprocessing

Data cleaning is a critical part of this project, as raw retail price data often contains inconsistencies.

3.1 Cleaning the Price Column

Prices were originally stored as strings (e.g., "£1.50", "£2–£3").

A custom function clean_item_price() was revisited and refined to:

Remove currency symbols (£)

Handle hyphenated price ranges by extracting the relevant numeric value

Convert cleaned values into floating-point numbers

This resulted in a new column:

item-price-fixed (numeric, float)

The original price column was retained for traceability.

3.2 Handling Hyphenated and Duplicate Values

Rows with hyphenated price values were inspected.

Consistency in the size column was used to justify extracting a single representative price.

Duplicate product entries were identified and removed to avoid skewing analysis.

3.3 Column Standardization

Column names were cleaned and standardized for clarity and usability.

Data types were validated to ensure numerical operations could be safely applied.

4. Exploratory Data Analysis (EDA)
4.1 Price Distribution by Category

The distribution of prices was examined across different product categories.

Density plots were used to understand how prices are spread rather than relying only on averages.

Why density plots?

They show the full distribution of prices.

They highlight clustering, skewness, and overlaps between categories.

5. Comparative Analysis: Everyday Value vs Branded
5.1 Feature Engineering

A new column was created to classify products into:

Everyday Value

Others (Branded)

This enabled a direct comparison between low-cost private labels and branded products.

5.2 Visualization Techniques Used
a) Density Plot

Used to compare price distributions between Everyday Value and Branded products.

Shows how frequently certain price ranges occur.

Observation:

Everyday Value products cluster heavily at the lower price range.

Branded products show a wider spread, extending into higher price points.

b) Box Plot

Used to summarize price distribution using median, quartiles, and outliers.

Why box plots?

They clearly show price variability.

They highlight differences in median prices and the presence of premium-priced items.

6. Key Inferences and Insights

Everyday Value products have:

A tight and consistent price distribution

Lower median prices

Minimal price variability

Branded products:

Exhibit a wider price range

Include premium-priced outliers

Reflect differentiated pricing strategies (branding, quality perception)

The analysis confirms a clear pricing strategy:

Everyday Value focuses on affordability and price stability

Branded products leverage perceived value to justify higher prices

These insights are directly relevant for:

Pricing strategy evaluation

Product portfolio optimization

Consumer behavior analysis

7. Tools and Techniques Summary

Python Libraries: Pandas, NumPy, Lets-Plot

Techniques Applied:

Data concatenation and ingestion

String parsing and numeric conversion

Duplicate handling

Feature engineering

Exploratory and comparative visualization

8. Conclusion

This project demonstrates a complete data analytics workflow—from raw data ingestion to actionable business insights. Through systematic cleaning, thoughtful visualization, and comparative analysis, the study successfully highlights pricing differences between Everyday Value and Branded bakery products.

The techniques used are scalable and transferable to other retail and supply-chain datasets, making this project a strong example of applied business analytics.
