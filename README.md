# 🎬 Movie Recommender System

A content-based movie recommender system built with **Python**, **Streamlit**, and the **OMDb API**. This app lets users select a movie and get 5 similar recommendations—complete with posters fetched in real-time.

---

## 📌 Features

- Recommend top 5 similar movies based on cosine similarity
- Fetch live movie posters using the OMDb API
- Streamlit-powered UI for ease of use

---

## 🛠 Tech Stack

- Python (Pandas, Scikit-learn, Pickle)
- Streamlit (for interactive web UI)
- OMDb API (for poster retrieval)

---

## 📁 Files

- `movie-recommender-system.ipynb`: Notebook to generate the similarity matrix
- `app.py`: Streamlit app to interact with the recommender
- `movies.pkl`: Serialized DataFrame with movie metadata
- `similarity.pkl`: Precomputed cosine similarity matrix

---

## 🧪 How to Run Locally

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/movie-recommender-system.git
cd movie-recommender-system
