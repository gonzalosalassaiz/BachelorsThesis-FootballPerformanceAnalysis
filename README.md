# ⚽ Football Performance Analysis Using Machine Learning

> Bachelor's Thesis — Analysis of professional football performance using Machine Learning

This repository contains the implementation of my Bachelor's Thesis in Computer Engineering, focused on the **analysis of professional football performance using Machine Learning techniques**.

The project explores how match event data can be transformed into meaningful performance metrics and subsequently used to build and evaluate predictive models.

---

## 📌 Overview

Football generates large amounts of event data that can be used to quantify team performance beyond traditional match statistics.

The main objective of this project is to investigate whether **match-level performance metrics extracted from event data can be used to model and predict goal difference**.

The project follows a complete data analysis and Machine Learning workflow:

```text
Football Event Data
        │
        ▼
Data Collection
        │
        ▼
Data Cleaning & Processing
        │
        ▼
Performance Metrics
        │
        ▼
Feature Engineering
        │
        ▼
Machine Learning Models
        │
        ▼
Model Evaluation
```

---

## 🎯 Objectives

The main objectives of the project are:

* Collect professional football event data.
* Explore and understand the available match and event information.
* Extract meaningful performance metrics from individual matches.
* Engineer features that represent different aspects of team performance.
* Investigate the relationship between performance metrics and goal difference.
* Train and evaluate different Machine Learning regression models.
* Compare model performance using quantitative evaluation metrics.
* Explore the impact of including team information as a feature.

---

## 📊 Data

The project uses football event data accessed through the [`statsbombpy`](https://github.com/statsbomb/statsbombpy) library and the StatsBomb open-data ecosystem.

The analysis starts by retrieving available competitions and matches and subsequently collecting the event data associated with individual matches.

The event-level dataset contains information about actions occurring during matches, which is then processed to construct team-level performance metrics.

### Performance Metrics

Among the metrics developed during the analysis are measures related to:

* ⚽ Goals
* 🎯 Shots
* 📈 Shot effectiveness
* 🏃 Team performance
* 🔄 Match events
* 📊 Other event-based performance indicators

The target variable used for the regression analysis is **goal difference**.

---

## 🤖 Machine Learning

Several regression approaches were implemented and evaluated.

### Linear Models

* Linear Regression
* Lasso Regression
* Lasso with Cross-Validation
* Ridge Regression
* Ridge with Cross-Validation
* Elastic Net
* Elastic Net with Cross-Validation

### Ensemble Models

* Random Forest Regressor
* Random Forest with Grid Search
* Random Forest with Randomized Search

The models are evaluated both **with and without team information**, allowing the analysis to investigate how categorical team information affects predictive performance.

---

## 🔬 Model Evaluation

The models are evaluated using several regression metrics, including:

| Metric  | Description                                                |
| ------- | ---------------------------------------------------------- |
| **R²**  | Measures the proportion of variance explained by the model |
| **MSE** | Mean Squared Error                                         |
| **MAE** | Mean Absolute Error                                        |

Cross-validation and hyperparameter optimization are also used for selected models.

For Random Forest, both `GridSearchCV` and `RandomizedSearchCV` are used to explore different hyperparameter configurations.

---

## 🛠️ Technologies

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/XGBoost-EC0000?style=for-the-badge&logo=xgboost&logoColor=white"/>
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge"/>
</p>

### Main Libraries

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical computing
* **Scikit-learn** — Machine Learning and model evaluation
* **XGBoost** — Gradient boosting
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **StatsBombpy** — Football event data access

---

## 📁 Repository Structure

```text
BachelorsThesis-FootballPerformanceAnalysis/
│
├── TFG_GonzaloSalasSaiz.py
│       └── Main analysis and Machine Learning implementation
│
├── MemoriaTFG_GonzaloSalasSaiz.pdf
│       └── Complete Bachelor's Thesis
│
└── README.md
        └── Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have Python 3.x installed.

Clone the repository:

```bash
git clone https://github.com/gonzalosalassaiz/BachelorsThesis-FootballPerformanceAnalysis.git
```

Navigate to the project:

```bash
cd BachelorsThesis-FootballPerformanceAnalysis
```

Install the main dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost statsbombpy
```

Run the analysis:

```bash
python TFG_GonzaloSalasSaiz.py
```

> **Note:** The project was originally developed as part of an academic thesis and contains exploratory analysis code. Some sections may require adaptation depending on the current version of the external data source and Python dependencies.

---

## 📄 Thesis

The complete Bachelor's Thesis is available in the repository:

**[📘 Read the full thesis](./MemoriaTFG_GonzaloSalasSaiz.pdf)**

The thesis provides the theoretical background, methodology, data analysis, Machine Learning approach and conclusions of the project.

---

## 🔍 Key Areas Explored

This project combines several areas that are relevant to modern data-driven software and AI applications:

```text
Data Collection
      ↓
Data Engineering
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
Machine Learning
      ↓
Model Selection
      ↓
Hyperparameter Optimization
      ↓
Model Evaluation
```

This makes the project a practical example of applying an end-to-end Machine Learning workflow to a real-world domain.

---

## 📚 Academic Context

This project was developed as my **Bachelor's Thesis in Computer Engineering**.

**Author:** Gonzalo Salas Saiz
**Degree:** Computer Engineering
**Project:** Football Performance Analysis Using Machine Learning

---

## 🔮 Future Improvements

Potential future developments include:

* Improving the feature engineering pipeline.
* Introducing more advanced football performance metrics.
* Incorporating additional competitions and seasons.
* Exploring player-level features.
* Applying more advanced Machine Learning algorithms.
* Investigating time-series approaches.
* Comparing additional ensemble methods.
* Developing a reproducible data pipeline.
* Building an interactive dashboard for model results.
* Deploying the resulting models as an API or cloud-based application.

---

## ⭐ About the Project

This project represents my first major end-to-end Machine Learning project, combining **Python, data analysis, feature engineering and predictive modelling** within a real-world domain.

It also serves as a foundation for my continued interest in **Software Engineering, Machine Learning and AI Engineering**.

---

<p align="center">
  <i>Turning football data into measurable insights through Machine Learning.</i>
</p>
