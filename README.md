# Personalized Movie Recommender System with Enhanced Accuracy Using Collaborative Filtering
 

 Movie Recommendation System
This repository provides code to build a movie recommendation system based on collaborative filtering, matrix factorization, and other techniques. The project uses data from zee-movies.dat, zee-ratings.dat, and zee-users.dat files to analyze movie ratings, user demographics, and movie details.

Table of Contents
Project Overview
Dataset Description
File Structure
Data Preprocessing
Recommendation System Methods
Evaluation Metrics
Installation
Usage
Contributing
License
Project Overview
This project implements a movie recommendation system that predicts user ratings and recommends movies based on collaborative filtering techniques. The system also uses techniques such as cosine similarity, k-nearest neighbors, singular value decomposition (SVD), non-negative matrix factorization (NMF), and collective matrix factorization.

Dataset Description
The project includes three main datasets:

Movies Dataset (zee-movies.dat): Contains movie metadata, including MovieID, Title, and Genres.
Ratings Dataset (zee-ratings.dat): Contains user ratings with UserID, MovieID, Rating, and Timestamp.
Users Dataset (zee-users.dat): Contains user demographic information, including UserID, Gender, Age, Occupation, and Zip-code.
File Structure
zee-movies.dat: Movie metadata file.
zee-ratings.dat: User ratings file.
zee-users.dat: User demographics file.
recommendation_system.ipynb: Main Jupyter notebook containing the code for loading data, preprocessing, building, and evaluating the recommendation system.
README.md: Project documentation.
Data Preprocessing
Reading Files:
Load the data using pd.read_fwf() with appropriate encoding.
Splitting and Renaming Columns:
Use str.split() to separate columns based on "::" and rename them for consistency.
Date Conversion:
Convert Timestamp to datetime format in the ratings data for temporal analysis.
Genre Extraction and Encoding:
Extract genres, handle variations in genre names, and encode genres as binary columns for easier analysis.
Merging Datasets:
Combine the users, movies, and ratings data to create a unified dataset for recommendation tasks.
Feature Engineering:
One-hot encoding for gender, and target encoding for Zip-code and Occupation based on average ratings.
Recommendation System Methods
Collaborative Filtering:

Calculate item and user similarities using cosine similarity.
Use NearestNeighbors for finding similar movies based on the ratings matrix.
Matrix Factorization:

Implemented using Collective Matrix Factorization (CMF) and Singular Value Decomposition (SVD).
Use Truncated SVD and NMF for dimensionality reduction and to approximate the ratings matrix.
Item-Based and User-Based Filtering:

Calculate cosine similarity for both item-item and user-user matrices.
Recommend items to users based on their similarity scores.
k-Nearest Neighbors (k-NN):

Build a k-NN model for item-based recommendations using brute-force cosine similarity.
Matrix Factorization with CMF:

Collective Matrix Factorization (CMF) to reduce dimensionality and provide a recommendation score matrix.


Evaluation Metrics
To assess the quality of recommendations, the following metrics are used:

Mean Squared Error (MSE):

Evaluates the difference between predicted and actual ratings.
Mean Absolute Percentage Error (MAPE):

Measures prediction accuracy relative to the actual ratings.

Usage
Open and run the recommendation_system.ipynb Jupyter notebook.
Modify parameters such as the number of recommendations, similarity metrics, and matrix factorization components as needed.
