# 🔵 Chicago Crime Arrest Prediction
### Predictive Modeling | Classification | Public Safety Analytics

---

## 📌 Problem Statement

**Can we predict whether a reported crime in Chicago will result in an arrest?**

This project builds a binary classification model to predict the `Arrest` outcome (Yes/No) for crimes reported in Chicago, using features such as crime type, location, time of day, and district. The goal is to uncover patterns that drive arrest likelihood and surface actionable insights for public safety stakeholders.
Notebook Link: https://colab.research.google.com/drive/1JL8CB0yPxGeTNDLyDfbXjtXBRbhIunqL#scrollTo=14568fba
---

## 🎯 Target Variable

| Variable | Type | Description |
|----------|------|-------------|
| `Arrest` | Boolean (True/False) | Whether the incident resulted in an arrest |

This is a **supervised binary classification** problem.

---

## 📂 Dataset

- **Source:** [Chicago Data Portal – Crimes 2001 to Present](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2)
- **Size:** 8+ million rows (sampled for modeling)
- **Format:** Tabular CSV
- **Maintained by:** City of Chicago (updated regularly)

### Key Features

| Feature | Description |
|---|---|
| `Date` | Date and time of the crime |
| `Primary Type` | Category of crime (e.g., THEFT, ASSAULT) |
| `Description` | Sub-category of the primary type |
| `Location Description` | Where the crime occurred (e.g., STREET, APARTMENT) |
| `District` | Chicago Police District |
| `Community Area` | Neighborhood identifier |
| `Latitude / Longitude` | Geospatial coordinates |
| `Arrest` | **Target variable** — whether an arrest was made |
| `Domestic` | Whether the crime was domestic-related |

---

## 💡 Why This Dataset?

The Chicago Crime Dataset was selected for the following reasons:

1. **Rich ecosystem** — Widely used in academic projects, Kaggle competitions, Medium tutorials, and GitHub repositories, providing ample reference material.
2. **Well-maintained** — Hosted on Chicago's official open data portal and updated regularly.
3. **Feature richness** — Contains temporal, geospatial, and categorical features ideal for feature engineering.
4. **Real-world impact** — Arrest prediction has direct implications for resource allocation, policing strategy, and criminal justice research.
5. **Scale** — Millions of rows allow robust modeling while sampling keeps compute manageable.

---

## 🌍 Domain Context & Use Case

**Domain:** Public Safety / Criminal Justice

Chicago's police department responds to hundreds of thousands of incidents annually. Understanding what factors correlate with arrests can help:

- **City planners** identify high-risk crime types and locations
- **Policy researchers** study disparities in arrest patterns by district or crime type
- **Operational analysts** optimize patrol and resource deployment

This model does **not** advocate for any particular policing strategy — it is an analytical tool for surfacing data-driven patterns.

---

## 📈 Potential Value of the Model

| Stakeholder | Decision-Making Impact |
|---|---|
| Chicago PD Leadership | Identify crime types with low arrest rates for resource review |
| Community Organizations | Understand which neighborhoods have arrest gaps |
| Researchers | Study time-of-day and seasonal patterns in arrest outcomes |
| Data Scientists | Benchmark dataset for classification techniques |

A well-calibrated model could serve as a baseline for fairness audits — examining whether arrest rates vary unexpectedly across geography or crime type after controlling for other factors.

---

## 🗂️ Project Structure

```
chicago-crime-arrest-prediction/
│
├── README.md                  ← You are here
├── notebook.ipynb             ← Main analysis notebook
├── data/
│   └── crimes_sample.csv      ← Sampled dataset (from Chicago Data Portal)
└── visuals/
    └── (generated plots)
```

---

## 🔬 Notebook Overview

The notebook (`notebook.ipynb`) is organized into the following sections:

### 1. Problem Definition
- Business framing
- Target variable identification
- Success metrics (accuracy, precision, recall, AUC-ROC)

### 2. Data Acquisition
- Loading data from the Chicago Data Portal
- Initial inspection (shape, dtypes, nulls)

### 3. Exploratory Data Analysis *(in progress)*
- Arrest rate by crime type
- Temporal patterns (hour of day, day of week, month)
- Geographic distribution (heatmap by district/community area)
- Domestic vs. non-domestic crimes

### 4. Feature Engineering *(planned)*
- Extract hour, day, month from `Date`
- Encode categorical variables
- Handle missing values

### 5. Modeling *(planned)*
- Baseline: Logistic Regression
- Tree-based: Random Forest, Gradient Boosting
- Evaluation: Confusion matrix, ROC curve, feature importance

### 6. Insights & Conclusions *(planned)*
- Top predictors of arrest
- Model limitations and ethical considerations

---

## 📊 Visualizations

> *Visualizations will be added as the project develops. Examples include:*

- **Arrest Rate by Primary Crime Type** — bar chart showing which crime types most/least often result in arrest
- **Heatmap by District** — geographic distribution of crimes and arrest rates
- **Time Series** — arrest rates by hour of day and day of week
- **Confusion Matrix** — model classification performance
- **ROC Curve** — AUC performance across classification thresholds
- **Feature Importance Plot** — top predictors from Random Forest model

---

## ⚙️ Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

---

## 📎 References

- [Chicago Data Portal – Crimes Dataset](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2)
- [Medium – Chicago Crime Analysis Tutorial](https://medium.com/)
- [Kaggle – Chicago Crime Datasets](https://www.kaggle.com/)

---

*Project developed for DS coursework — Spring 2026*
