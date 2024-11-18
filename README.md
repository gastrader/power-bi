# Data Analysis and Visualization of the DataCo Smart Supply Chain Dataset

## Overview  
This project focuses on analyzing and visualizing the [DataCo Smart Supply Chain dataset](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis). The goal is to clean, manipulate, and create interactive visualizations to track key metrics, including sales and shipping performance, while enabling year-based filtering.

---

## Objectives  
1. **Data Preparation**: Clean and preprocess the data for analysis.  
2. **Key Metrics**:
   - **Sales by Country**.
   - **On-Time Rate (OTR)** of shipping.
   - OTR broken down by **Country** and **Shipping Mode**.
   - **Order breakdown (On-Time vs. Late)** by Quarter.
3. **Dynamic Filtering**: Allow users to filter all graphs by `Order Year`.

---

## Steps  

### 1. Data Exploration  
- Load the dataset and inspect its structure.
- Key columns used:
  - `order date (DateOrders)`
  - `Sales`
  - `Delivery Status`
  - `Late_delivery_risk`
  - `Shipping Mode`
  - `Order Country`
- Convert date columns (e.g., `order date (DateOrders)`) to `datetime` for time-based analysis.

### 2. Data Cleaning  
- **Handle missing values**:
  - Check for nulls in critical columns like `Sales` and `Delivery Status`.
  - Impute or drop rows/columns based on relevance.
- **Standardize data**:
  - Rename columns for clarity.
  - Convert data to appropriate types (e.g., numerical, categorical).
- **Generate new columns**:
  - Extract `Order Year` and `Quarter` from `order date (DateOrders)`.
  - Create `On-Time` and `Late` categories based on shipping metrics.

### 3. Data Manipulation  
- Aggregate data by:
  - **Country** for sales and on-time rate.
  - **Shipping Mode** for OTR analysis.
  - **Quarterly trends** for order breakdown.
- Calculate:
  - **Total Sales**: Sum of the `Sales` column.
  - **On-Time Rate (OTR)**: `(On-Time Orders / Total Orders) * 100`.

### 4. Visualization  
Create interactive, filterable charts to explore key metrics:

#### Graphs:
1. **Sales by Country**  
   - Bar chart of total sales by country with color-coded performance.  

2. **On-Time Rate (OTR) Trends**  
   - Line chart displaying OTR over time, filterable by year.  

3. **OTR by Country**  
   - Scatter plot comparing OTR by country, highlighting outliers.  

4. **OTR by Shipping Mode**  
   - Stacked bar chart showing OTR for `Standard Class`, `First Class`, `Second Class`, and `Same Day`.  

5. **Order Breakdown (On-Time vs. Late)**  
   - Pie or area chart showing the proportion of on-time vs. late orders by quarter.

### 5. Dynamic Filtering  
Enable slicers or dropdowns to filter by `Order Year`, updating all visualizations dynamically.
![powerbi](https://github.com/user-attachments/assets/ba854bc8-b0aa-4ea1-bc50-6b74a830117e)

Now filter the visuals by 2016:
![powerbi2](https://github.com/user-attachments/assets/68a14e5a-e681-4d6c-ac7d-da5e4ed92a39)

---
