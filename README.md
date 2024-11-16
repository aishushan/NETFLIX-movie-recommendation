# Netflix Movie Recommendation System

## Project Overview
This project implements a **Netflix Movie Recommendation System** using content-based filtering. The system recommends movies or TV shows based on their similarities derived from key features such as title, director, cast, description, and other relevant columns in the dataset. This approach uses **TF-IDF Vectorization** for text feature extraction and **Cosine Similarity** to measure the similarity between items.

The dataset used in this project is a collection of Netflix movies and TV shows with various details such as title, director, cast, release year, rating, and more. The model recommends movies/shows that are similar to a given title based on content features.


## Objective
The goal of this project is to create a recommendation system that suggests movies or TV shows based on user input. The system:
- Preprocesses the Netflix dataset by handling missing data and cleaning the content.
- Extracts features using **TF-IDF Vectorization**.
- Computes the similarity between movies using **Cosine Similarity**.
- Provides the top 10 recommendations for any given movie/show from the dataset.

## Data Preprocessing
The dataset was cleaned and preprocessed by:
- Removing irrelevant columns from the dataset.
- Filling missing values with appropriate defaults (e.g., "No Director", "No Cast").
- Creating a combined feature column from several key attributes (e.g., title, director, cast, description).
- Dropping unnecessary columns to focus on important information.

## Model Development
The recommendation system uses:
1. **TF-IDF Vectorization**: Converts text data into numerical form by weighing words based on their frequency across documents.
2. **Cosine Similarity**: Measures the cosine of the angle between two vectors, indicating their similarity.

This method allows the system to recommend movies or TV shows that are similar to a given input title.

## Recommendation Function
The function `get_recommendations()` takes a movie/show title and finds the most similar items based on the cosine similarity of their features. The system returns the top 10 most similar movies or TV shows, excluding the input title itself.

For example, when querying the title **'Blood & Water'**, the function returns similar titles like:
1. Diamond City
2. Kings of Jo'Burg
3. Shirkers
...

## Deployment
To make the recommendation system accessible:
1. The cleaned data and recommendation function were saved using **joblib** for easy reuse.
2. The recommendation system is deployed using **Streamlit**, allowing users to interact with the model via a web interface.

Users can input a movie/show title and receive personalized recommendations.

## Files for Download:
- **cleaned_df.pkl**: Contains the preprocessed and cleaned dataset.
- **recommendation_function.pkl**: Contains the trained recommendation function.
