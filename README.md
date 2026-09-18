# Olist: Where Should Delivery Improvement Begin?

This is my B106 Data Visualisation project from Gisma University. Just putting it here.

I used the Brazilian E-Commerce Public Dataset by Olist to see where delivery problems actually start. This is mostly for people who work in operations or care about customer experience and want to know which times or places or delivery steps they should look at first.


* Name: Divakar Sabarwal
* Student ID: GH1047352
* Module: B106 Data Visualisation
* Lecturer: Mehran Monavari

# Business question

Where should Olist even start to figure out why deliveries go wrong and people leave bad reviews?

I started by looking at how late deliveries and bad reviews are connected, then checked if it changes by month, by region, by product type, and by delivery step. I just found out what to look at first, not saying what causes what or how much money it saves.

# Dataset

I used the Brazilian E-Commerce Public Dataset by Olist for this.
There are about 100,000 orders from Brazil in this dataset, from 2016 to 2018. The download has nine CSVs but I only used six:

* olist_orders_dataset.csv
* olist_customers_dataset.csv
* olist_order_reviews_dataset.csv
* olist_order_items_dataset.csv
* olist_products_dataset.csv
* product_category_name_translation.csv

Each row is one order. But in the item and review tables, the same order ID can show up more than once because one order can have many items or reviews.

# Project files

Data Visualisation Final Project/
├── README.md
├── Data_visualisation_project.ipynb   # Main analysis notebook
├── brief.md                           # Assessment-brief notes
├── data/                              # Original Olist CSV files

Don’t change the original CSV files. All the paths in the notebook are from the main project folder.

# Libraries

I just used the libraries we learned in class:

* pandas
* NumPy
* Matplotlib
* Seaborn
* Streamlit is imported in the notebook but I didn’t actually use it for a separate app.

# Running the notebook

1. Download the Olist dataset and put the CSVs in the data/ folder. Don’t rename them.
2. Open the project folder in Jupyter Notebook or JupyterLab.
3. Open Data_visualisation_project.ipynb.
4. Restart the kernel and run all the cells from top to bottom.
5. Check if the data tables and all five charts show up without any errors.


# Analysis workflow

Here’s how I did it step by step:

1. Define the audience, business problem and analytical scope.
2. Load and inspect the relevant CSV files.
3. Audit table sizes, missing values, duplicate rows, data types and value ranges.
4. Convert dates, select one review per order and create one order-level analytical table.
5. Define late delivery and poor-review measures using explicit denominators.
6. Present five explanatory visual insights.
7. Provide recommendations, limitations and a conclusion.

# Main insights

1. Late deliveries and bad reviews: 62.4% of late orders got a 1 or 2 star review, but only 9.3% of on-time ones did. If I only look at reviews sent after delivery, the late-order rate drops to 19.4%, so it’s not all cause and effect.
2. Monthly pattern: Late deliveries were highest in March 2018 at 19%, then dropped a lot in April.
3. Regional stuff: Rio de Janeiro had a lot of orders and also more late deliveries and bad reviews than other places.
4. For all five big product categories, Rio de Janeiro had the most bad reviews out of the high-volume states.
5. Late orders spend more time after the carrier takes over, so maybe that’s where the real problem is.

# Visual design

There are five charts in the notebook: bar, line, scatter, heatmap, and box plot. I used different shades of red to highlight important stuff. All the rates and shares are in percentages so it’s easier to compare.

# Important limitations

* This data is old, from 2016 to 2018, so it’s not what’s happening right now.
* I’m just looking at the data, so I can’t say late deliveries actually cause bad reviews.
* Some reviews were sent in before the delivery was even recorded.
* I left out any orders or reviews that didn’t have the info I needed.
* Comparing regions or categories might also be affected by different sellers, products, times, or customers.
* The carrier handoff times just split up the delivery steps, but they don’t show exactly where the delay happened.

# References

The Olist dataset is published on Kaggle the link is provided in the jupiter notebook.