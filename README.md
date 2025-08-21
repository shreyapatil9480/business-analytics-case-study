# Business Analytics Project

## Overview

This repository contains a **synthetic business dataset** and an accompanying Jupyter notebook designed to showcase core analytical skills relevant to **business analyst**, **program manager**, and **data analyst** roles. The project is organized as follows:

* A **CSV dataset** (`data/business_data.csv`) simulating monthly business performance metrics across regions.
* An **analysis notebook** (`analysis.ipynb`) that walks through exploratory data analysis (EDA), visualizations, and predictive models for revenue forecasting and profitability classification.
* A `requirements.txt` file listing Python packages used in the notebook so you can easily reproduce the results.

This repository is ready to use out of the box: clone it, install the dependencies, and open the Jupyter notebook to explore the data and analysis.

## Synthetic Dataset

The dataset is stored in `data/business_data.csv` and contains **500 rows** with the following columns:

| Column | Type | Description |
| --- | --- | --- |
| `Month` | Integer | Month of the year (1–12). |
| `Season` | Categorical | Season corresponding to the month: `Winter`, `Spring`, `Summer`, or `Autumn`. |
| `Marketing_Spend` | Integer | Amount spent on marketing for the month. |
| `Economic_Index` | Float | Simulated economic health indicator (higher values indicate stronger economic conditions). |
| `Competition_Index` | Float | Simulated measure of competitive pressure (higher values indicate more competition). |
| `Product_Price` | Float | Average selling price of the product. |
| `Sales_Volume` | Integer | Number of units sold. |
| `Returned_Items` | Integer | Number of units returned by customers. |
| `Customer_Satisfaction` | Integer | Customer satisfaction score (1–10). |
| `Region` | Categorical | Geographic region: `North`, `South`, `East`, or `West`. |
| `Revenue` | Float | Calculated revenue = `Product_Price × (Sales_Volume − Returned_Items)`. |
| `Profit` | Float | Calculated profit = `Revenue − Marketing_Spend`. |
| `Is_Profit` | Binary | Indicator (1 or 0) showing whether the scenario is profitable (`Profit > 0`). |

The data are **synthetic**—generated programmatically to mimic realistic patterns—so you can freely use and modify them without privacy concerns.

## Notebook Contents

The notebook `analysis.ipynb` demonstrates a typical workflow for analyzing business data:

1. **Data loading and initial inspection:** Read the CSV file using pandas and view its shape and first few rows.
2. **Descriptive statistics:** Summarize numeric and categorical columns to understand central tendencies and variation.
3. **Exploratory visualizations:** Plot distributions of key variables, scatter plots to explore relationships (e.g., marketing spend vs. revenue), and a correlation heatmap to identify linear associations.
4. **Regression modeling:** Apply linear regression to predict `Revenue` using marketing spend, economic/competition indices, pricing, and other predictors. The notebook uses `scikit‑learn` to split the data, scale features, fit a model, and report the mean squared error.
5. **Classification modeling:** Use logistic regression to predict the binary `Is_Profit` label. The notebook encodes categorical variables, trains a model, and evaluates it with accuracy and a classification report.
6. **Conclusions:** Summarize insights from the analysis and model performance, highlighting how such techniques can inform business decisions.

The notebook is executed and saved with output cells, so you can read it directly in GitHub or run it locally to reproduce the results.

## Getting Started

1. **Clone the repository:**

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME
```

2. **Create a Python environment (optional but recommended):**

```bash
python3 -m venv venv
source venv/bin/activate
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

4. **Launch Jupyter Notebook:**

```bash
jupyter notebook analysis.ipynb
```

Follow the notebook to explore the data, run the cells, and reproduce the analysis. You can modify the notebook to test additional models, adjust parameters, or explore new visualizations.

## Contributing

You are welcome to fork this repository or open a pull request if you have ideas for enhancing the dataset, analysis, or visualizations. Adding other models (e.g., decision trees, random forests), tuning hyperparameters, or creating interactive dashboards would be great next steps.

## License

This project is released under the MIT License. See `LICENSE` for details.

