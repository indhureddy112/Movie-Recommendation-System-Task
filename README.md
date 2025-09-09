# Movie-Recommendation-System-Task
This project builds a content-based movie recommendation system using Python, Pandas, Scikit-learn, and NLP techniques. It recommends movies based on similarity of genres, keywords, cast, crew, and overview.
Features
       Preprocesses raw movie dataset (merged_movies.csv)

       Extracts important features: overview, genres, keywords, cast, crew

       Normalizes text (lowercasing, removing spaces)

       Combines features into a single tags column

       Uses CountVectorizer (Bag of Words) for text vectorization

       Computes cosine similarity matrix between movies

       Provides a recommend() function to suggest top 10 similar movies

       Saves preprocessed dataset and trained model using pickle
Data preprocessing steps 
        Load Dataset → Select required columns (movie_id, title, overview, genres, keywords, cast, crew).

        Handle Missing Values → Remove rows with missing data.

        Parse JSON-like Strings → Convert genres, keywords, cast, crew from stringified JSON to lists.

        Extract Top Features:

                  Top 3 cast members

                  Director (from crew)

        Clean Text → Lowercase, remove spaces, split overview.

        Create Tags Column → Merge overview + genres + keywords + cast + crew.

        Save Preprocessed Dataset → Store as preprocessed_movies.csv.
Model  training 
         Vectorization → Convert tags into numerical vectors using                                      
         CountVectorizer(max_features=5000, stop_words='english').

         Similarity Matrix → Compute cosine similarity across all movie vectors.

         Save Model → Store DataFrame (movies.pkl) and similarity matrix (similarity.pkl).
         Output (sample):

🎬 Top 10 recommendations for 'Avatar':
1. Guardians of the Galaxy
2. John Carter
3. The Helix... Loaded
4. Star Trek Into Darkness
5. Aliens
6. Independence Day
7. Avatar: The Way of Water
8. The Matrix
9. Star Wars
10. Jupiter Ascending
