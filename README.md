### Movie Recommender System

This is a movie recommender system built using Python, Dataset contains information of over 45,000 movies. The system utilizes movie metadata such as genres, keywords, cast, and crew to recommend similar movies based on text similarity. Below is a breakdown of the system's functionalities:

#### Dataset

- It is available on Kaggle (https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

#### Importing Dependencies

- The necessary libraries (`numpy`, `pandas`) are imported to handle data manipulation and preprocessing.

#### Data Preprocessing

- The system preprocesses movie metadata by loading data from CSV files (`movies_metadata.csv`, `credits.csv`, `keywords.csv`), merging datasets, and cleaning the data.
- Columns like `genres`, `keywords`, `cast`, and `crew` are formatted and processed to extract relevant information.

#### Stemming

- Stemming is applied to text data to reduce words to their root form, enhancing text similarity calculations. The Porter Stemmer from NLTK library is used for this purpose.

#### Text Vectorization

- The system converts text data into numerical vectors using CountVectorizer, which represents the frequency of words in the text.
- Cosine similarity is calculated between vectors to determine the similarity between movies based on their metadata.

#### Recommender Functionality

- The `recommend()` function takes a movie title as input and returns a list of top 5 recommended movies based on similarity scores.
- It utilizes cosine similarity scores to find the most similar movies to the input movie.

#### Using the System

- To utilize the system, simply call the `recommend()` function with the title of the movie for which recommendations are sought.

#### Example Usage:

```python
recommend('Movie Name')
```

Replace `'Movie Name'` with the title of the movie for which you want recommendations.

#### Note:

- This system relies on movie metadata and text similarity, providing recommendations based on textual features.
- The effectiveness of recommendations may vary based on the quality and relevance of metadata and the similarity calculation method.
