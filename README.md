# Football Performance Analysis Using Machine Learning

<p align="center"><strong>End-to-end analysis of professional football performance using event data and machine learning</strong></p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" alt="Python">
<img src="https://img.shields.io/badge/Machine%20Learning-scikit--learn-orange?logo=scikitlearn" alt="Machine Learning">
<img src="https://img.shields.io/badge/Data-StatsBomb-green" alt="StatsBomb">
<img src="https://img.shields.io/badge/Status-Academic%20Project-informational" alt="Status">
</p>

## Overview

This repository contains the implementation developed for a **Bachelor's Thesis on professional football performance analysis using machine learning**.

The project combines **StatsBomb event data**, football performance metrics, exploratory data analysis, regression models, hyperparameter tuning and model evaluation to study the relationship between team actions during a match and **goal difference**.

The original analysis was developed from a Google Colab workflow and is preserved in `TFG_GonzaloSalasSaiz.py`.

## Objectives

- Collect professional football match and event data.
- Build team-level performance metrics from event data.
- Use **goal difference** as the target variable.
- Compare several regression approaches.
- Evaluate models using standard regression metrics.
- Study the relationship between football performance indicators and the target variable.
- Analyze the effect of including team identity as a feature.

## Data

The project uses the public **StatsBomb Open Data** ecosystem through [`statsbombpy`](https://github.com/statsbomb/statsbombpy).

The analysis currently works with these competitions/seasons:

- UEFA Euro 2024
- Copa America 2024
- Africa Cup of Nations 2023
- FIFA World Cup 2022
- UEFA Euro 2020

The workflow retrieves match information and detailed event data and combines them into analysis-ready pandas DataFrames.

> **Data note:** StatsBomb data is subject to its own terms and attribution requirements. This repository contains the analysis code; it does not redistribute the underlying event dataset.

## Analysis Pipeline

```text
StatsBomb competitions
        ↓
Match data
        ↓
Event data
        ↓
Feature engineering
        ↓
Team-level performance metrics
        ↓
Train / test split
        ↓
Regression models
        ↓
Hyperparameter tuning
        ↓
Model evaluation
        ↓
Interpretation & visualisation
```

## Performance Metrics

The analysis derives multiple indicators from football event data, including:

- Shot efficiency
- Expected goals (xG)
- Carry duration
- Opponent shots in dangerous areas
- Dangerous set-piece actions
- Possession effectiveness
- Passes leading to shots
- Dangerous passes
- Successful dribbles
- High-press recoveries
- Progressive passes
- Defensive actions

These features are combined at team/match level and used to model goal difference.

## Machine Learning

The repository experiments with several regression approaches.

### Linear Models

- Linear Regression
- Lasso
- LassoCV
- Ridge
- RidgeCV
- Elastic Net
- ElasticNetCV

### Tree-Based Models

- Random Forest Regressor
- XGBoost Regressor

### Hyperparameter Optimisation

- GridSearchCV
- RandomizedSearchCV
- Cross-validation

### Evaluation Metrics

Models are evaluated using:

- **R²**
- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- Cross-validated R²

The repository intentionally does not hard-code a headline model score in this README: results depend on the data returned by the StatsBomb API, installed package versions and the exact execution environment.

## Repository Structure

```text
.
├── TFG_GonzaloSalasSaiz.py
├── MemoriaTFG_GonzaloSalasSaiz.pdf
├── README.md
├── requirements.txt
└── .gitignore
```

| File | Description |
|---|---|
| `TFG_GonzaloSalasSaiz.py` | Main analysis and machine learning workflow |
| `MemoriaTFG_GonzaloSalasSaiz.pdf` | Bachelor's Thesis report |
| `requirements.txt` | Python dependencies |
| `.gitignore` | Standard Python/IDE/OS exclusions |

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/gonzalosalassaiz/BachelorsThesis-FootballPerformanceAnalysis.git
cd BachelorsThesis-FootballPerformanceAnalysis
```

### 2. Create a virtual environment

Linux/macOS:

```bash
python -m venv .venv
source .venv/bin/activate
```

Windows:

```powershell
python -m venv .venv
.venv\\Scripts\\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the analysis

The main script was originally generated from a **Google Colab/Jupyter workflow** and contains notebook-specific commands. For the current version, the recommended execution environment is **Google Colab or Jupyter**.

Open `TFG_GonzaloSalasSaiz.py` and execute the workflow in a notebook-compatible environment.

> A future refactor can convert the current monolithic workflow into a standard Python package with separate modules for data acquisition, feature engineering, modelling and evaluation.

## Thesis

The complete academic report is available in `MemoriaTFG_GonzaloSalasSaiz.pdf`.

## Engineering Roadmap

The current repository preserves the original thesis implementation. The next engineering iteration can evolve it into a more maintainable ML project:

- [ ] Separate data acquisition from feature engineering.
- [ ] Move reusable transformations into dedicated modules.
- [ ] Introduce configuration for competitions and seasons.
- [ ] Add automated tests for feature calculations.
- [ ] Add reproducible experiment configuration.
- [ ] Store model evaluation results in structured outputs.
- [ ] Add model interpretation and feature-importance analysis.
- [ ] Add a small CLI for running the pipeline.
- [ ] Add CI for linting and tests.
- [ ] Improve reproducibility with pinned dependency versions.

## Academic Context

**Bachelor's Thesis — Computer Engineering**

The project was developed as an applied machine learning study focused on football analytics, combining data engineering, exploratory analysis, feature engineering and supervised learning.

---

If you are interested in football analytics, machine learning or reproducible data science workflows, feel free to explore the implementation and the accompanying thesis.
