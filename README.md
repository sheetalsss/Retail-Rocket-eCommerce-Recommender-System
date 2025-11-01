# Retail Rocket eCommerce Recommender System

A comprehensive analysis of e-commerce customer behavior and product recommendations using Jupyter notebooks.

## Dataset Description

The analysis uses three main CSV files:

- **events.csv**: User interactions (views, add to cart, transactions)
- **category_tree.csv**: Product category hierarchy  
- **item_properties.csv**: Item attributes and characteristics

## Key Features

### Customer Segmentation
- Total unique visitors: 1,407,580
- Purchasing customers: 11,719 (0.83% conversion rate)
- Browsing-only customers: 1,395,861

### User Journey Analysis
Tracks customer paths from viewing → add to cart → purchase
Example user journey shown with timestamps and item interactions

### Recommendation System
Simple collaborative filtering implementation:
```python
def recommender_bought(item_id, purchased_items):
    recommender_list = []
    for x in purchased_items:
        if item_id in x:
            recommender_list += x
    return list(set(recommender_list) - set([item_id]))
```

## Customer Feature Engineering

Created dataset with:

visitorid, num_items_viewed, view_count, bought_count, purchased

### Notebook Structure

- Data Loading & Exploration
    - Import datasets
    - Understand data structure and columns
    - Event Analysis

- Transaction vs browsing behavior
    - User journey mapping
    - Product Analysis

- Category tree relationships
    - Item properties examination
    - Customer Segmentation

- Purchasers vs browsers
    - Feature engineering for clustering
    - Recommendation System

### "Customers who bought this also bought" implementation

### Key Insights

- Very low conversion rate (0.83%)
- Complex multi-step user journeys
- Clear behavioral patterns between customer segments
- Foundation for basket analysis and recommendations

## Requirements

- bash
- pandas
- numpy 
- matplotlib
- seaborn

## Usage

Run the Jupyter notebook sequentially to reproduce the analysis and generate insights for e-commerce optimization.
