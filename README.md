# AI Movie Recommender System

A **content-based movie recommender system** built using machine learning and deployed as an interactive **Streamlit web application**.  
The system recommends movies based on **content similarity** using cosine similarity and allows users to apply **advanced filters** for better recommendation quality.

---

##  Features

- Content-based recommendation using **Cosine Similarity**
- Movie similarity computed from:
  - Overview
  - Genres
  - Keywords
  - Cast
  - Director
- Advanced filters:
  - Minimum IMDb rating
  - Release year range
- Explainable recommendations with **similarity score**
- Clean and minimal Streamlit UI
- Uses **OMDb API** for posters and movie metadata

---

## How the Recommendation Works

1. Movie metadata is processed and combined into a single **tags** feature.
2. Text data is vectorized using **CountVectorizer**.
3. **Cosine similarity** is calculated between movie vectors.
4. For a selected movie:
   - Top similar movies are retrieved
   - Filters are applied (rating & year)
   - Results are displayed with similarity score

> The similarity score represents how close two movies are in feature space.

---

## Similarity Score Explanation

- Calculated using **cosine similarity**
- Value range: `0 → 1`
- Higher score = more similar content
- Absolute values may be low due to high-dimensional sparse vectors  
  (ranking matters more than magnitude)

---

## Tech Stack

- Python
- Pandas & NumPy
- Scikit-learn
- Streamlit
- OMDb API

---

## Dataset

Source: **TMDB 5000 Movie Dataset (Kaggle)**

- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

---


