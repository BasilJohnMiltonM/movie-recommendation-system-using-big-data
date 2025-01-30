**Movie Recommendation System**

**Overview**

This project is a Big Data Movie Recommendation System implemented using Apache Spark. The system leverages collaborative filtering techniques to generate movie recommendations based on user ratings. The project is built using PySpark and executed in Google Colab with a distributed computing environment.

This project was completed as part of the MSBA program for the course IDS 561 - Analytics for Big Data.
This project is a Big Data Movie Recommendation System implemented using Apache Spark. The system leverages collaborative filtering techniques to generate movie recommendations based on user ratings. The project is built using PySpark and executed in Google Colab with a distributed computing environment.

**Features:**

Big Data Processing: Utilizes Apache Spark for handling large-scale movie rating data.

Collaborative Filtering: Implements Alternating Least Squares (ALS) and User-Based Collaborative Filtering recommendation models.

Data Analysis & Visualization: Analyzes user behavior, genre popularity, and movie trends using Matplotlib & Seaborn.

Google Colab Integration: Runs on Google Colab with Spark setup.

**Dataset**

The project uses the MovieLens dataset, which contains:

movies.csv: Movie details (title, genres, movieId)

ratings.csv: User ratings for movies (userId, movieId, rating, timestamp)

tags.csv: User-assigned tags for movies

**Technologies Used**

Python (pandas, matplotlib, seaborn)

Apache Spark (PySpark, MLlib)

Google Colab (for cloud execution)

Big Data Processing (Distributed computation with Spark)

**Installation & Setup**

Clone the repository:

git clone https://github.com/your-username/Movie-Recommendation-System.git
cd Movie-Recommendation-System

Install dependencies:

pip install findspark pyspark pandas matplotlib seaborn

Run Jupyter Notebook or Google Colab.

**Steps in the Project**

1. Environment Setup

Mounted Google Drive

Installed Apache Spark 3.5.0

Configured Spark environment

2. Data Loading & Exploration

Loaded datasets (movies.csv, ratings.csv, tags.csv)

Inspected schema, checked missing values & duplicates

Explored movie ratings distribution, genre popularity, and user activity

3. Data Preprocessing

Cleaned missing values and duplicates

Converted genres into separate rows for better analysis

Merged movies and ratings for recommendation modeling

4. Visualization & Insights

User Activity: Distribution of user ratings

Genre Popularity: Most-rated and best-rated genres

Movie Ratings Distribution: Number of ratings per movie

Correlation Analysis: Relationship between movie popularity and rating

5. Building the Recommendation System

Implemented Alternating Least Squares (ALS) Collaborative Filtering from Spark MLlib

Implemented User-Based Collaborative Filtering using similarity measures

Trained the models using ratings.csv

Generated movie recommendations for users

Evaluated using RMSE (Root Mean Square Error) and Precision-Recall metrics

**Results & Findings**

* Popular movies tend to have lower average ratings due to a large number of diverse opinions.

* Less popular movies with niche audiences often receive higher ratings, indicating strong user affinity for specific genres or content.

* Highly active users (who rate many movies) play a significant role in the recommendation system, as their preferences help shape collaborative filtering.

* Comedy and Drama are the most frequently rated genres, while niche genres like Documentary and Film-Noir have fewer but often highly rated entries.

* The ALS model performed well in personalized recommendations, especially for users with a higher number of ratings.

* User-Based Collaborative Filtering provided additional insights by recommending movies based on user-user similarity.

* There is a strong correlation between movies with a high number of ratings and their overall rating variance, meaning that the more people rate a movie, the more polarized the ratings can be.

* Cold Start Problem: New users and movies with very few ratings tend to receive less accurate recommendations. This could be improved with hybrid filtering techniques.

**Future Enhancements**

Add content-based filtering using NLP on movie descriptions.

Improve model tuning with hyperparameter optimization.

Deploy as a web application for interactive recommendations.

Combine ALS and user-based filtering for a hybrid recommendation system.

