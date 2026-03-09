# Spotify Song Recommendation System  
## CountVectorizer vs TF-IDF Comparison

### Project Overview
This project implements a **content-based music recommendation system** using Natural Language Processing (NLP) techniques. The system recommends songs similar to a given input song by analyzing song metadata such as artist name, album, and explicit flag. The goal of this project is to compare two text vectorization techniques — **CountVectorizer** and **TF-IDF** — and evaluate how each method affects recommendation quality.

### Dataset
The dataset used in this project is **spotify_tracks.csv**, which contains metadata for songs including:
- Song name
- Artist name
- Album
- Explicit

These features are combined into a single text representation that is used for vectorization.

### Methodology
1. **Data Preprocessing**
   - Loaded dataset using Pandas
   - Selected relevant columns
   - Handled missing values
   - Combined metadata features into one text feature

2. **Feature Vectorization**
   - **CountVectorizer**: Converts text into numerical vectors based on word frequency.
   - **TF-IDF Vectorizer**: Converts text into numerical vectors based on term importance across the dataset.

3. **Similarity Calculation**
   - Cosine similarity is used to measure similarity between songs.
   - Songs with higher cosine similarity values are considered more similar.

4. **Recommendation Generation**
   - User provides a song name.
   - The system finds the song in the dataset.
   - Cosine similarity scores are calculated with all other songs.
   - Songs are sorted by similarity score.
   - Top N similar songs are recommended.

### Model Evaluation
The models were evaluated by calculating the **average cosine similarity score of the top recommendations**.

| Model | Average Similarity Score |
|------|--------------------------|
| CountVectorizer | **0.46** |
| TF-IDF | **0.31** |

### Conclusion
The results show that **CountVectorizer performed better than TF-IDF for this dataset**. This is because the dataset contains short categorical text fields such as artist names and album titles. CountVectorizer preserves token frequency effectively for such data, while TF-IDF is typically more suitable for longer textual documents.

### Technologies Used
- Python  
- Pandas  
- Scikit-learn  
- Natural Language Processing  
- Cosine Similarity  


### Key Learnings
- Building a **content-based recommendation system**
- Understanding differences between **CountVectorizer and TF-IDF**
- Using **cosine similarity for similarity-based recommendations**
- Feature engineering for NLP tasks
- Evaluating recommendation algorithms

---
### Author
**Anusree**
