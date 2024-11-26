# Movie Recommender System
This project is a simple movie recommendation system that utilizes user ratings and a correlation matrix to suggest movies based on user preferences. It uses data from the MovieLens dataset and employs pandas and NumPy to process and analyze the data.

# Introduction
The recommendation system uses collaborative filtering to suggest movies. By analyzing user ratings and finding correlations between movies, it identifies films that are similar to those rated highly by a user. The system emphasizes:

- Popularity-based filtering with a minimum number of ratings.
- Weighted scores to enhance recommendations based on user preferences.

# Features 
- Reads and processes user ratings and movie details.
- Builds a pivot table to create a user-item matrix.
- Computes a correlation matrix for movies based on user ratings.
- Generates personalized movie recommendations for users.

# Dataset 
The project uses the MovieLens 100k dataset, which contains:

-u.data: User ratings for movies (columns: User Id, Movie_ID, Rating).
-u.item: Movie metadata (columns: Movie_ID, Movie_title).
These files are preprocessed and merged to build the recommendation engine.

# How It Works
1 Load and Merge Data:
- User ratings (u.data) are combined with movie details (u.item).
2. Create a User-Item Matrix:
- A pivot table is built with rows as user IDs and columns as movie titles, with the ratings as values.
3. Compute Correlation Matrix:
- A Pearson correlation is calculated between all movies.
- A minimum number of ratings (min_periods) is applied to filter unpopular movies.
4. Generate Recommendations:
- For a selected user, the system identifies similar movies based on the correlation matrix and the user’s preferences.
- Scores are weighted by user ratings to enhance personalization.
