# Product-Level Retail Demand Forecasting

This repository contains the implementation supporting an MSc dissertation on **weekly product-level retail demand forecasting**.

The study compares statistical, machine-learning and deep-learning forecasting approaches under the same chronological evaluation framework.

## Models

- Naive
- Seasonal Naive
- Linear Regression
- XGBoost
- Long Short-Term Memory (LSTM)
- ARIMA

## Research design

The workflow includes:

1. data-quality inspection and cleaning;
2. UK-market selection and product-eligibility filtering;
3. weekly product-level demand panel construction;
4. lag, rolling-statistic and calendar feature engineering;
5. chronological training, validation and final-test splits;
6. model development and time-aware validation;
7. rolling one-step-ahead final evaluation;
8. pooled and product-level performance analysis.

The primary metric is **RMSE**, with **MAE** and **sMAPE** reported as complementary measures.

## Dataset

This project uses the **Online Retail II** dataset:

> Chen, D. (2012). *Online Retail II* [Dataset]. UCI Machine Learning Repository.  
> DOI: `10.24432/C5CG6D`

The raw dataset is **not redistributed** in this repository.

Download the official dataset from the UCI Machine Learning Repository and place the Excel file at:

```text
data/online_retail_II.xlsx
```

The notebook also supports the common Google Colab fallback path:

```text
/content/online_retail_II.xlsx
```

## Repository contents

```text
retail-demand-forecasting-thesis/
├── README.md
├── online_retail_forecasting.ipynb
└── requirements.txt
```

## Reproducibility

The notebook documents the main analysis pipeline, including data cleaning, weekly aggregation, feature engineering, model development, validation and final-test evaluation.

Random seed `42` is used where applicable. TensorFlow deterministic operations are enabled where possible; exact deep-learning results may still vary slightly across hardware and low-level software environments.

## Running the notebook

Create an environment and install the required packages:

```bash
pip install -r requirements.txt
```

Then place the dataset in the expected path and run the notebook from top to bottom.

For Google Colab, upload the dataset to `/content/online_retail_II.xlsx` before running the data-loading cells.

## Dissertation scope

The contribution is **empirical and comparative**, rather than the proposal of a new forecasting algorithm. The analysis examines both pooled forecasting accuracy and product-level model suitability across demand characteristics.

## Author

Turgay Mert Erdem  
MSc Data Science, AI & Digital Business  
GISMA University of Applied Sciences
