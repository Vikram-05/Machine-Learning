# Movie Recommendation System using NLP

## Project Overview
This project implements a content-based movie recommendation system using Natural Language Processing (NLP) techniques. The system analyzes movie metadata (titles, overviews, taglines, and genres) to find and recommend similar movies to users.

## Dataset
- **Source**: `movies_metadata.csv`
- **Description**: A comprehensive dataset containing movie information including titles, overviews, taglines, genres, vote counts, and popularity scores

## Methodology

### 1. Data Loading and Preprocessing
- Load the movie metadata CSV file
- Select relevant columns: `title`, `overview`, `tagline`, `genres`, `vote_count`, `popularity`
- Handle missing values by filling with empty strings
- Parse the JSON-formatted genres column to extract genre names

### 2. Feature Engineering
- Combine title, overview, tagline, and genres into a single `tags` column
- This consolidated text representation captures multiple aspects of each movie

### 3. Text Preprocessing (NLP)
The system applies comprehensive text cleaning:
- **Tokenization**: Break text into individual words using NLTK
- **Lemmatization**: Convert words to their base form (e.g., "running" → "run")
- **Stopword Removal**: Eliminate common English words that don't add value
- Apply POS (Parts of Speech) tagging for accurate lemmatization

### 4. Vectorization
- **TF-IDF (Term Frequency-Inverse Document Frequency)**: Convert text to numerical vectors
- Limit to top 5000 features for computational efficiency
- This captures the importance of each word relative to the entire corpus

### 5. Similarity Computation
- **Cosine Similarity**: Measure the similarity between movie vectors
- Generates a similarity matrix comparing all movies
- Higher scores indicate more similar content

## Key Functions

### `recommendation(title, max_size=10)`
Recommends movies similar to the input movie.

**Parameters:**
- `title` (str): Name of the movie to find recommendations for
- `max_size` (int): Number of recommendations to return (default: 10)

**Returns:**
- List of recommended movie titles

**Example Usage:**
```python
recommedation('toy story')
# Returns: Top 10 movies similar to 'Toy Story'
```

## Implementation Details

### Libraries Used
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical operations
- **nltk**: Natural Language Processing (tokenization, lemmatization, stopword removal)
- **scikit-learn**: TF-IDF vectorization and cosine similarity computation
- **seaborn**: Data visualization

### Data Processing Steps
1. Fill null values in title, tagline, and overview with empty strings
2. Parse JSON-formatted genres to extract genre names
3. Create a combined text field from multiple columns
4. Apply lemmatization and stopword removal to the combined field
5. Generate TF-IDF vectors for all movies
6. Create an index mapping movie titles to their row indices

## Results
The system successfully recommends similar movies based on:
- Plot similarity (overview content)
- Genre alignment
- Thematic elements (from taglines)
- Movie metadata

## Advantages of Content-Based Approach
- No need for user rating data
- Handles new movies immediately
- Provides explainable recommendations based on content similarity
- Language-independent to some extent

## Potential Improvements
- Incorporate user ratings and collaborative filtering
- Add user preference weighting
- Implement ensemble methods combining multiple similarity metrics
- Use advanced NLP models (Word2Vec, BERT) for better text representations
- Include director, cast, and production company information
- Add temporal aspects (release date, trends)
