# 🎌 Anime Recommendation System in Python

![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg)
![Status](https://img.shields.io/badge/status-active-success)

> A hybrid anime recommender using Content-Based and Collaborative Filtering in Python.

---

## 📌 Table of Contents

- [📂 Dataset](#dataset)
- [🚀 Features](#features)
- [🛠️ Installation](#installation)
- [▶️ How to Run](#how-to-run)
- [📜 Credits](#credits)

---

## 📂 Dataset

We use the **Anime Recommendation Database** from [MyAnimeList on Kaggle](https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database), which includes:

- `anime.csv` — metadata of ~12,000 anime
- `rating.csv` — ~7.8 million user-anime interactions

---

## 🚀 Features

### ✅ Data Preprocessing
- Removed missing values and duplicates
- Cleaned and standardized genre data
- Normalized ratings using `MinMaxScaler`

### 🧠 Content-Based Filtering (CBF)
- Uses TF-IDF and cosine similarity on genre text
- Recommends similar anime based on selected title

### 👥 Collaborative Filtering (CF)
- Uses SVD (Singular Value Decomposition) from the `Surprise` library
- Learns user preferences from past ratings

### 🔗 Hybrid Recommendation System
- Combines CBF and CF based on user history
- Falls back to CBF for new users (cold start)

### 📊 Visualizations
- Bar charts of top-rated anime
- Histograms of user rating distribution
- Interactive recommendation widgets in Jupyter

---

## 🛠️ Installation

Install required packages:

```bash
pip install -r requirements.txt

---
## 📜 Credits

- **Dataset**: [Anime Recommendation Database – Kaggle](https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database)
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `surprise`, `streamlit`, `ipywidgets`
- **Creator**: Guduru Manasa


