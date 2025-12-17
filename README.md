# 📱 Sentiment Scope: E-Commerce Review Analyzer

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> **Turning 60,000+ raw customer reviews into actionable business intelligence.**

---

## 📖 Overview

In the competitive world of e-commerce, customer feedback is gold—but only if you can understand it at scale. **Sentiment Scope** is an end-to-end Machine Learning solution designed to analyze "Cell Phones and Accessories" reviews.

It moves beyond simple star ratings, using **Natural Language Processing (NLP)** to understand the *why* behind the sentiment. The project tackles real-world messy data, handles severe class imbalance, and delivers a robust engine for flagging negative feedback.

---

## 🚀 Key Features

### 1. 🧹 Advanced Data Engineering (Part I)
Data doesn't come clean. This project features a rigorous cleaning pipeline:
* **Smart Imputation:** Handled missing price data by calculating *brand-specific* averages (e.g., Apple vs. Nokia prices) rather than global averages, preserving data integrity.
* **Metadata Merging:** Enriched user reviews with product metadata (Price, Brand, Category) for deeper insights.
* **Exploratory Analysis:** Uncovered top-selling brands, price distributions, and the inherent "Positive Bias" in online reviews (75% Positive / 25% Negative).

### 2. 🧠 The NLP Engine (Part II)
A custom-built text processing factory that prepares raw text for machine learning:
* **Normalization:** Lowercasing, contraction mapping (`won't` → `will not`), and noise removal.
* **Lemmatization:** Reducing words to their semantic root to improve model generalization.
* **Vectorization:** Utilizing Bag-of-Words (CountVectorizer) to transform text into mathematical features.

### 3. ⚖️ Solving Class Imbalance
The biggest challenge? The dataset was heavily skewed toward positive reviews. A standard model would simply guess "Positive" and get high accuracy but fail to catch complaints.
* **The Fix:** implemented **Random Oversampling**.
* **The Result:** Balanced the training data (50/50), forcing the model to learn the nuances of negative reviews.

---

## 📊 Results & Performance

We trained a **Multinomial Naive Bayes** classifier. Here is the impact of our optimization strategy:

| Metric | Baseline Model | Optimized Model (Oversampled) | Impact |
| :--- | :---: | :---: | :--- |
| **Accuracy** | ~86% | ~85% | Slight Trade-off |
| **Specificity** (Catching Negatives) | **58%** | **82%** | **🚀 +24% Improvement** |

> **Business Win:** The Optimized Model is significantly better at identifying unhappy customers, allowing support teams to intervene proactively.

---

## 📂 Project Structure

| File | Description |
| :--- | :--- |
| `Solution+Part-I.ipynb` | **Data Preparation & EDA:** Loading data, cleaning missing values, merging datasets, and visual analysis. |
| `Solution+Part-II.ipynb` | **NLP & Modeling:** Text preprocessing pipeline, model training (Naive Bayes), oversampling, and evaluation. |

---

## 🛠️ Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (Naive Bayes, RandomOverSampler)
* **NLP:** NLTK (WordNetLemmatizer, Stopwords)

---
