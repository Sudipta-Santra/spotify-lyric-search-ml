# Spotify Lyric Search – Machine Learning Project

## Project Overview
Spotify Lyric Search is a machine learning and NLP-based project that identifies the **Song Title** and **Artist** from a small snippet of song lyrics.  
The system simulates a real-world scenario where a user remembers only a few lines of a song and wants to identify it.

This project is intentionally designed to be **simple, explainable, and interview-friendly**, focusing on core NLP concepts rather than complex deep learning models.

---

## Problem Statement
Given a short text snippet from song lyrics, predict:
- The corresponding **Song Title**
- The **Artist**

---

## Technologies Used
- Python  
- Pandas  
- Scikit-learn  
- NLTK  

---

## Dataset
- Spotify 50k+ Songs Dataset  
- Each row represents one song  
- Columns used:
  - `artist` – Artist name
  - `song` – Song title
  - `text` – Full song lyrics

---

## Approach & Methodology

### 1. Text Preprocessing
- Convert lyrics to lowercase
- Remove punctuation and special characters
- Remove stop-words using NLTK  
This ensures the model focuses only on meaningful words.

### 2. Feature Extraction
- TF-IDF Vectorization
- Uses **unigrams and bigrams** to capture both single words and meaningful phrases
- Converts lyrics into numerical vectors based on word importance

### 3. Similarity-Based Prediction
- Cosine similarity is used to compare the user’s lyric snippet with all songs in the dataset
- The song with the highest similarity score is selected as the prediction

---

## Why TF-IDF Instead of Deep Learning?
- Lyrics are highly unique, making similarity-based methods very effective
- TF-IDF is fast, interpretable, and computationally efficient
- Deep learning would be unnecessary and harder to explain for this task
- This approach follows the principle: *use the simplest model that works well*

---

## User Input Flow
- The user enters a lyric snippet at runtime
- The input text is preprocessed and vectorized
- The model returns the predicted **song name** and **artist**

---

## Model Evaluation
- Random lyric snippets are extracted from the dataset
- Snippets are matched against the full lyrics
- Accuracy is measured using **Top-1 similarity matching**

**Achieved Accuracy:** ~85% to 95%

This evaluation method closely represents real-world usage.

---

## Project Structure

spotify-lyric-search/

  │
  
  ├── Spotify Lyric Search - Machine Learning Project.ipynb
  
  ├── Spotify Million Song Dataset_exported.zip
  
  └── README.md

---
### Sample Input
you are the dancing queen young and sweet only seventeen


### Sample Output
Song   : Dancing Queen

Artist : ABBA

---
## Conclusion
This project demonstrates how traditional NLP techniques like TF-IDF and cosine similarity can effectively solve real-world text identification problems. By prioritizing simplicity and explainability, the solution achieves strong performance while remaining easy to understand and maintain.

