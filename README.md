# Music Recommendation System

## Overview

This project aims to build a music recommendation system that can recommend songs based on user preferences. By understanding the relationships between various musical features and user preferences, this project also aims to provide insights for artists about the evolution of music and its reception.

## Motivation

We wanted to address the shortcomings of existing music recommendation apps and build a model that can recommend music more effectively based on the data we have. Our main questions were:

- Why are some music recommendation apps bad?
- How can we build a better music recommendation system?
- What hidden relationships exist between music features that indicate user preferences?

## Datasets

1. **Main Dataset**: Contains over 170,000 songs with 19 features such as artist, genre, and popularity. Key features include valence, acousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, and tempo.
2. **Genre Dataset**: Classifies each song into detailed genres and calculates the mean value of each feature for each genre, with nearly 3,000 different genres.

## Data Processing and Visualization

- **Correlation Matrix**: Showed positive correlations between year and popularity, energy and loudness, and danceability and valence. Negative correlations were observed between acousticness and energy/year.
- **Standardization and PCA**: Applied to the numeric data, with 15 principal components identified. Acousticness contributed most to PC1, and duration contributed most to PC2.

## Models and Techniques

- **Clustering**: Used K-means clustering on the genre dataset and the year dataset, visualizing clusters of similar genres and years.
- **Recommendation Algorithm**: Based on cosine distance between the mean feature vectors of user-selected favorite songs and all songs in the dataset. The closest songs are recommended, filtering out those already in the user’s input.

## Performance

- **Recommendations**: Tested by selecting favorite songs and evaluating the recommendations. Results varied, with some successful recommendations and some limitations in diversity.
- **Limitations**: The system tended to recommend similar songs repeatedly. Future improvements could include filtering out duplicate recommendations, introducing randomness for diversity, and combining content-based and collaborative filtering approaches.

## Conclusion

Our content-based filtering algorithm showed potential for recommending music based on song characteristics. However, for better diversity and accuracy, integrating collaborative filtering and possibly using NLP for lyric analysis would be beneficial. This project was a collaborative effort, with each member contributing to different aspects, from data processing to building and testing the recommendation system.