**Tata 1mg Product Catalog Analysis**

This project is a deep dive into the product catalog of Tata 1mg, a leading online pharmacy. The goal was to take a raw, web-scraped dataset and transform it into a fully interactive Power BI dashboard that uncovers insights into product performance, pricing strategies, and brand positioning.

# Project Objective

I wanted to move beyond simple data presentation and create a tool for analysis. The dashboard is designed to answer key business questions like:

  * What are our most popular products, and what makes them successful?
  * Is there a relationship between a product's price and its customer rating?
  * Which brands dominate our catalog, and how do they perform?
  * How can we identify "best value" products for our customers?

# The Process

The entire project was handled within Power BI, from data cleaning to the final report.

1. Data Cleaning & Transformation (Power Query): The initial dataset was messy. Key cleaning steps included:

      * Parsing text from numeric columns like `price`, `rating`, and `rating_count`.
      * Extracting meaningful information from the `pack_size` column to create new `Pack Type` and `Quantity` columns.
      * Engineering a `Brand Name` column by splitting the product `Name`.

2. Feature Engineering (DAX & Power Query):To get deeper insights, I created several new columns:

      * Discount & Discount Percentage:Calculated to analyze pricing strategies.
      * Popularity Score: A custom formula `[rating] * LOG([rating_count] + 1)` was created to provide a more balanced measure of popularity than just the average rating alone. This score rewards products that have both a high rating and a significant number of reviews to back it up.
      * Rating Tier: A conditional column to categorize products as "Excellent," "Good," or "Average."

# Dashboard Features

The final report is a two-page interactive dashboard:

Product Overview: This is the main dashboard that gives a high-level view of the entire catalog. It features key KPIs, a "Best-Sellers" chart (based on the custom popularity score), and an analysis of how pricing, ratings, and discounts relate to each other.

Brand Details: This page is a dedicated deep-dive tool. A user can select any brand from a slicer to see a detailed breakdown of its product portfolio, average rating vs. the competition, and a full list of its products.

This project was a great exercise in taking a real-world, messy dataset and building a polished, insightful, and user-friendly analytical tool from scratch.
