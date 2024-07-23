# Movie Recommender System

This project is a movie recommender system that suggests movies to users based on their ratings and the similarities between movies. The system uses collaborative filtering and k-nearest neighbors (KNN) to find and recommend similar movies to users.

## Introduction

The movie recommender system is designed to suggest movies to users based on their past ratings. It uses collaborative filtering and KNN to find movies that are similar to those the user has rated highly.

## Data Description

The system uses two datasets:

1. `ratings.csv` - Contains user ratings for different movies.
2. `movies.csv` - Contains information about the movies.

## Installation

To run this project, you need to have Python installed along with the following libraries:

- pandas
- numpy
- scipy
- scikit-learn

if you are using Jupyter Notebok environment than you will get these already installed.

## Code Explanation
### Data Exploration and Preparation
The first step involves exploring the data and preparing it for analysis:

- Counts the number of ratings, unique movies, and unique users.
- Calculates average ratings per user and per movie.
- Identifies the lowest and highest-rated movies based on average ratings.
- Creating the User-Item Matrix
- We create a sparse matrix representation of the user-item interactions using the csr_matrix from scipy.sparse. This matrix is essential for efficient computation, especially with large datasets.

### Finding Similar Movies
We define a function find_similar_movies that uses the k-nearest neighbors (KNN) algorithm to find movies similar to a given movie. The function returns a list of movie IDs that are similar to the given movie.

### Recommending Movies to Users
We define a function recommend_movies_for_user that recommends movies to a user based on their highest-rated movie. The function prints the recommended movies based on the user's preferences.

### Example Usage
The code provides an example of recommending movies to a user with ID 150. It finds the highest-rated movie by this user and recommends 10 similar movies.
