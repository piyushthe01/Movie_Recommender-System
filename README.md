# 🎬 Movie Recommender System

A content-based movie recommender app built with **Python**, **Streamlit**, and the **OMDb API**. Select a movie and get personalized recommendations with poster previews and similarity scores.

---

## 📌 Features

- Recommend top N similar movies based on cosine similarity.  
- Fetch live movie posters via OMDb API (with caching).
- Responsive, themed UI with search and slider controls.
- Handles missing posters gracefully.

---

## 🛠 Tech Stack

- **Python** (Pandas, Scikit-learn)
- **Streamlit** (UI)
- **Requests** (API calls)
- **Pickle** (data serialization)

---

## 📂 Dataset

This project uses the **TMDB 5000 Movies Dataset** from Kaggle:  
🔗 [https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

The `movies.pkl` and `similarity.pkl` files are generated using the processing and vectorization steps in the Jupyter notebook (`movie-recommender-system.ipynb`).  
If you'd like to recreate or modify the data pipeline, please refer to that notebook.

---

## 📂 Repository Structure

```
├── app.py                   # Streamlit entry point
├── movies.pkl               # Movie metadata (use Git LFS or external storage)
├── similarity.pkl           # Precomputed similarity matrix (use Git LFS or external storage)
├── movie-recommender-system.ipynb  # Notebook for data prep
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

---

## 🚀 Handling Large Data Files

Since `movies.pkl` and `similarity.pkl` exceed GitHub’s 25 MB limit, choose one of the following approaches:

1. **Git LFS (Large File Storage)**
   - Install Git LFS:
     - macOS: `brew install git-lfs`
     - Ubuntu: `sudo apt-get install git-lfs`
     - Windows: Download from [git-lfs.github.com](https://git-lfs.github.com/)
   - Initialize and track large files:
     ```bash
     git lfs install
     git lfs track "*.pkl"
     git add .gitattributes
     git add movies.pkl similarity.pkl
     git commit -m "Track large files with Git LFS"
     git push origin main
     ```

2. **External Storage**  
   - Upload `movies.pkl` and `similarity.pkl` to cloud (Google Drive, AWS S3, Dropbox) and make them publicly accessible.
   - Modify `load_data()` in `app.py` to download them at runtime if not found locally.

3. **Data Versioning with DVC**  
   - Install DVC: `pip install dvc`
   - Initialize DVC: `dvc init`
   - Add files: `dvc add movies.pkl similarity.pkl`
   - Commit generated `.dvc` files and push data to remote storage.

---

## 🧪 How to Run Locally

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/movie-recommender-system.git
   cd movie-recommender-system
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. **Set up large data files** using Git LFS or external storage (see above).
4. Add your OMDb API key in `app.py`:
   ```python
   OMDB_API_KEY = "YOUR_OMDB_KEY"
   ```
5. Run the app:
   ```bash
   streamlit run app.py
   ```

---

## 📬 Get OMDb API Key

Register at [OMDb API](https://www.omdbapi.com/apikey.aspx) for a free key and replace the placeholder in `app.py`.

---

## ✨ Future Improvements

- Deploy on Streamlit Cloud with secret management.  
- Add genre and year filters.  
- Enhance similarity using NLP embeddings (TF-IDF, BERT).  

---

Made with ❤️ by [Your Name]  
🌐 [linkedin.com/in/mishrapm](https://linkedin.com/in/mishrapm)
