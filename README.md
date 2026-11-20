# Content-Based Movie Recommendation System

A content-based movie recommendation engine built using Python, Scikit-Learn, and Gradio on the TMDB 5000 Movie Dataset. Given a movie title, the system recommends the top 5 most similar movies along with match percentages and genres.

## Features
- **Metadata Enrichment:** Combines plot overview, genres, top 3 cast members, and director into a unified text profile for each movie.
- **NLP Vectorization:** Uses TF-IDF Vectorizer (max_features=5000, English stop-words removed) to convert text metadata into numerical feature vectors.
- **Similarity Ranking:** Computes pairwise Cosine Similarity across 4,800+ movies to retrieve the closest matches.
- **Interactive Web UI:** Deployed an interactive dropdown interface using Gradio for real-time recommendations.

## Tech Stack
- **Language:** Python
- **Data Manipulation:** Pandas, AST
- **Machine Learning / NLP:** Scikit-Learn (TfidfVectorizer, cosine_similarity)
- **UI & Environment:** Gradio, Google Colab

## How It Works
1. Merged `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` and handled missing values.
2. Parsed JSON string columns to extract genres, top-3 cast, and director, removing spaces in names so multi-word names act as single tokens.
3. Built a TF-IDF matrix and calculated Cosine Similarity scores between movies.
4. Connected the recommendation function to a Gradio dropdown interface for live testing.

## How to Run
1. Download the TMDB 5000 Movie Dataset (`archive.zip`) from Kaggle.
2. Open `movie_recommender_system.ipynb` in Google Colab or Jupyter Notebook.
3. Upload the dataset, run all cells, and launch the Gradio interface.
