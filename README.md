# Olist: Where Should Delivery Improvement Begin?

This repository contains my B106 Data Visualisation individual project at Gisma University of Applied Sciences.

**Repository:** https://github.com/sabarwaldivakar/Data-Visualisation-final-project

The project uses the Brazilian E-Commerce Public Dataset by Olist to investigate where delivery-performance improvements should begin. The analysis is written for operations and customer-experience managers who need to decide which periods, regions and delivery stages deserve further investigation.

## Author

- **Name:** Divakar Sabarwal
- **Student ID:** GH1047352
- **Module:** B106 Data Visualisation
- **Lecturer:** Mehran Monavari

## Business question

With limited investigation capacity, where should Olist focus first to understand delivery problems and poor customer reviews?

The notebook moves from the overall relationship between delivery lateness and poor reviews to monthly patterns, regional differences, product categories and delivery stages. The findings identify priorities for investigation; they do not prove causation or estimate financial savings.

## Dataset

The project uses the [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

The dataset contains approximately 100,000 anonymised marketplace orders from Brazil between 2016 and 2018. The original download contains nine CSV files. This analysis uses six of them:

- `olist_orders_dataset.csv`
- `olist_customers_dataset.csv`
- `olist_order_reviews_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_products_dataset.csv`
- `product_category_name_translation.csv`

One analytical row represents one order. Item and review tables can contain repeated order IDs because an order may contain multiple items or review records.

## Project files

```text
Data Visualisation Final Project/
├── README.md
├── Data_visualisation_project.ipynb   # Main analysis notebook
├── Data_visualisation_project.html    # Self-contained final export
├── PROJECT_PLAN.md                    # Working plan and quality checks
├── brief.md                           # Assessment-brief notes
├── data/                              # Original Olist CSV files
├── references/                        # Assessment reference notes
└── backups/                           # Earlier notebook and plan versions
```

The raw CSV files should remain unchanged. All notebook paths are relative to the project folder.

## Libraries

The notebook uses methods and libraries covered in the module:

- pandas
- NumPy
- Matplotlib
- Seaborn
- Streamlit is currently imported in the notebook, although the submitted notebook analysis does not require a separate Streamlit application.

## Running the notebook

1. Download the Olist dataset and keep the original CSV filenames inside the `data/` folder.
2. Open the project folder in Jupyter Notebook or JupyterLab.
3. Open `Data_visualisation_project.ipynb`.
4. Restart the kernel and run all cells from top to bottom.
5. Check that the data tables and all five charts appear without errors.

If the libraries are not installed, they can be installed with:

```bash
python3 -m pip install pandas numpy matplotlib seaborn streamlit jupyter
```

## Analysis workflow

The notebook follows this structure:

1. Define the audience, business problem and analytical scope.
2. Load and inspect the relevant CSV files.
3. Audit table sizes, missing values, duplicate rows, data types and value ranges.
4. Convert dates, select one review per order and create one order-level analytical table.
5. Define late delivery and poor-review measures using explicit denominators.
6. Present five explanatory visual insights.
7. Provide recommendations, limitations and a conclusion.

## Main insights

1. **Late deliveries and poor reviews:** 62.4% of late orders received a 1–2-star review, compared with 9.3% of on-time orders. A review-timing sensitivity check reduces the late-order rate to 19.4% among reviews submitted after delivery, so the full difference should not be interpreted as a causal effect.
2. **Monthly pattern:** the late-delivery rate peaked at 19.0% for orders purchased in March 2018 before falling sharply in April.
3. **Regional priority:** Rio de Janeiro combines substantial reviewed-order volume with relatively high late-delivery and poor-review rates.
4. **Category consistency:** Rio de Janeiro has the highest poor-review rate across each of the five major product categories displayed among the selected high-volume states.
5. **Delivery stages:** late orders spend a larger share of their delivery journey after carrier handoff, suggesting that post-handoff events should be investigated first.

## Visual design

The notebook contains five charts: a bar chart, line chart, scatter plot, 5×5 heatmap and box plot. They use a restrained red colour family, with darker red drawing attention to important values. Rates and stage shares are expressed as percentages to make comparisons across differently sized groups more meaningful.

## Important limitations

- The data covers historical Brazilian marketplace orders from 2016–2018 and should not be treated as current operational evidence.
- The analysis is observational and cannot prove that delivery lateness causes poor reviews.
- Some reviews were submitted before recorded delivery.
- Delivery and review analyses exclude records without the required outcomes.
- Regional and category comparisons may also reflect seller, product, time-period or customer differences.
- Carrier-handoff timestamps divide the recorded journey but do not identify the exact source of a delay.

## Current status

The final notebook contains five completed insights and has been executed from top to bottom using the original CSV files. Its 19,714 Markdown-and-code source characters remain below the brief's stated 20,000-character limit under this counting method. The self-contained HTML export includes all code, tables, five charts and the clickable GitHub repository link.

Final deliverables:

- [`Data_visualisation_project.ipynb`](Data_visualisation_project.ipynb)
- [`Data_visualisation_project.html`](Data_visualisation_project.html)
- [`data/`](data/)

## Licence and attribution

The Olist dataset is published on Kaggle under the CC BY-NC-SA 4.0 licence. Full Harvard-style references for the dataset and relevant module materials are included in the notebook.
