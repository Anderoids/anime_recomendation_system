# 🎌 Anime Recommendation System in Python 

![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg)
![Status](https://img.shields.io/badge/status-active-success)

> A hybrid anime recommender using Content-Based + Collaborative Filtering in Python.

Welcome to the **Anime Recommendation System** project!  
This intelligent system recommends anime to users using a **hybrid approach** combining:

- 🎨 **Content-Based Filtering (CBF)** using TF-IDF & Cosine Similarity  
- 📈 **Collaborative Filtering (CF)** using Surprise’s SVD  
- 🧠 **Hybrid Recommendation System** that adapts based on user history  
- 📊 **Interactive Dashboard** with `ipywidgets` and visualizations  
- 🔥 **Top-5 Visualized Recommendations** per user or anime title

---

## 📂 Dataset

We use the **Anime Recommendation Database** (from [MyAnimeList](https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database)) consisting of:

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

## 🛠️ How to Run

### ⚙️ Environment Setup

```bash
pip install pandas numpy seaborn matplotlib scikit-learn ipywidgets wordcloud surprise
---

Credits
Dataset: Kaggle - Anime Recommendation Database
---

Libraries: pandas, scikit-learn, surprise, ipywidgets, seaborn, matplotlib, wordcloud
---

## License
This project is licensed under the MIT License
