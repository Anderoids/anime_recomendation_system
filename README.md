![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg)
![Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/github/license/Anderoids/anime_recomendation_system?color=blue)

>  A hybrid anime recommender using Content-Based + Collaborative Filtering in Python.

---

## 📌 Table of Contents

- [📌 Table of Contents](#-table-of-contents)
- [📂 Dataset](#dataset)
- [🚀 Features](#features)
- [🛠️ Installation](#installation)
- [▶️ How to Run](#how-to-run)
- [📊 Visualizations](#visualizations)
- [📜 Credits](#credits)
- [📄 License](#license)
- [💌 Contact](#contact)

---

## 📂 Dataset

> We use the **Anime Recommendation Database** (from [MyAnimeList on Kaggle](https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database)) consisting of:

- `anime.csv` — metadata of ~12K anime
- `rating.csv` — ~7.8M user-anime interactions

---

## 🚀 Features
### ✅ Data Preprocessing
- Removed duplicates and missing values
- Cleaned genres, converted to lowercase and unified format
- Normalized ratings using `MinMaxScaler`

### 🧠 Content-Based Filtering (CBF)
- TF-IDF Vectorization of genres
- Cosine similarity matrix for finding similar anime
- Function: `recommend_anime("Naruto", anime_df, cosine_sim)`

### 👥 Collaborative Filtering (CF)
- Matrix factorization with `SVD` from `Surprise`
- Trained on user-item interactions
- Function: `get_top_recommendations(user_id, model, anime_df, n=5)`

### 🔗 Hybrid Recommendation System
- Combines CF (if user history exists) and CBF (cold-start fallback)
- Function: `hybrid_recommend(user_id, anime_name, n=5)`

### 📊 Visualizations
- Bar plot of top-rated anime
- User rating distribution histogram
- Ranked hybrid recommendations bar chart
- Function: `plot_top_5_recommendations(user_id, anime_name, n=5)`

### 🧩 Interactive Dashboard (Jupyter Notebook)
- Uses `ipywidgets` for user input
- Dynamic visual output
- Fully integrated with CF/CBF models
---

## 🛠️ Installation

Install dependencies:

```bash
pip install -r requirements.txt
▶️ How to Run
📒 Jupyter Notebook
bash
Copy
Edit
jupyter notebook your_notebook_name.ipynb
🖥️ Streamlit App (if applicable)
bash
Copy
Edit
streamlit run app.py
📊 Visualizations
Feature	Description
📈 Bar Charts	Top-rated items
📉 Histograms	User rating distribution
📌 Interactive Widgets	User ID & Anime input
📍 Hybrid Output	Personalized + Similar titles

📜 Credits
Dataset: Dataset Name - Kaggle

Libraries: pandas, numpy, matplotlib, surprise, seaborn, streamlit, etc.

Creator: Guduru Manasa

📄 License
This project is licensed under the MIT License — see the LICENSE file for details.
