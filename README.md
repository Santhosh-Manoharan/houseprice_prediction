# House Price Prediction

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Dataset](https://img.shields.io/badge/Dataset-CSV-orange)](HousePricePrediction.csv)

> A machine learning project to predict residential house prices using regression
> techniques on structured real-estate data.

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [Results](#results)
- [License](#license)

---

## Overview

This project builds a regression model that predicts the sale price of a house
based on features such as lot area, building type, year built, overall condition,
basement square footage, and exterior covering. It follows a typical data-science
workflow: exploratory data analysis (EDA), feature engineering, model training,
evaluation, and comparison of multiple algorithms.

---

## Dataset

The dataset (`HousePricePrediction.csv`) contains **1,460** residential property
records with the following key columns:

| Column          | Description                                      |
|-----------------|--------------------------------------------------|
| `Id`            | Unique identifier                                |
| `MSSubClass`    | Building class                                   |
| `MSZoning`      | General zoning classification                    |
| `LotArea`       | Lot size in square feet                          |
| `LotConfig`     | Lot configuration                                |
| `BldgType`      | Type of dwelling                                 |
| `OverallCond`   | Overall condition rating (1&ndash;10)            |
| `YearBuilt`     | Original construction year                       |
| `YearRemodAdd`  | Remodel year                                     |
| `Exterior1st`   | Exterior covering                                |
| `BsmtFinSF2`    | Type 2 finished basement square feet             |
| `TotalBsmtSF`   | Total basement square feet                       |
| `SalePrice`     | **Target** — property sale price in USD          |

---

## Tech Stack

| Category        | Tool / Library                                     |
|-----------------|----------------------------------------------------|
| Language        | Python 3.9+                                        |
| Notebooks       | Jupyter Notebook                                   |
| Data Processing | pandas, NumPy                                      |
| Visualization   | Matplotlib, Seaborn                                |
| ML Models       | scikit-learn (Linear Regression, Random Forest, …) |
| Environment     | pip / venv                                         |
| CI / CD         | GitHub Actions                                     |

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/Santhosh-Manoharan/houseprice_prediction.git
cd houseprice_prediction
```

### 2. Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate   # Linux / macOS
.venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Launch the notebook

```bash
jupyter notebook houseprice_prediction.ipynb
```

### 5. Run the cells

Execute the notebook cells in order — the notebook walks through data loading,
EDA, preprocessing, model training, and evaluation.

---

## Project Structure

```
houseprice_prediction/
├── .github/
│   └── workflows/
│       └── ci.yml              # GitHub Actions CI pipeline
├── .gitignore                  # Python / ML gitignore rules
├── HousePricePrediction.csv    # Dataset
├── LICENSE                     # MIT License
├── README.md                   # Project documentation
├── houseprice_prediction.ipynb # Main Jupyter notebook
└── requirements.txt            # Pinned Python dependencies
```

---

## Results

After training and comparing multiple regression models (Linear Regression,
Random Forest, Gradient Boosting, etc.), the best-performing model achieves:

- **RMSE:** ~29,000 – 35,000 (depending on feature engineering)
- **R² Score:** ~0.85 – 0.90

*Run the notebook to reproduce and refine these results.*

---

## License

This project is licensed under the **MIT License** — see the
[LICENSE](LICENSE) file for details.
