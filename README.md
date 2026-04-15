# AkiSh98s-DSA210-repo
# 🎵 What Makes a Song Popular? – Spotify Data Analysis

##  Project Overview

This project aims to analyze the relationship between musical features and song popularity using Spotify data. The main goal is to understand which audio characteristics distinguish high-popularity songs from low-popularity songs.

The project follows the data science pipeline including:

* Data collection
* Exploratory Data Analysis (EDA)
* Hypothesis testing

---

## Dataset

The dataset is obtained from Kaggle:

https://www.kaggle.com/datasets/solomonameh/spotify-music-dataset

It consists of two separate CSV files:

* High popularity songs
* Low popularity songs

Each dataset contains multiple audio features such as:

* energy
* danceability
* loudness
* acousticness
* instrumentalness
* tempo
* valence (if available)

---

## Data Collection

The data was imported into Python using Pandas. Since the dataset is publicly available and already structured, the focus was on loading, inspecting, and preparing the data for analysis.

The datasets were checked for:

* Missing values
* Column consistency
* Data types

---

## !! Important Note About File Paths (Google Colab)

If you are running this project on Google Colab, file paths may differ.

Sometimes uploaded files appear with:

* `/mnt/data/...`
* or with `(1)` added to filenames

For example:

* `high_popularity_spotify_data.csv`
* `high_popularity_spotify_data(1).csv`

To avoid errors, the project uses a flexible loading function:

```python
SEARCH_DIRS = [".", "/mnt/data"]
```

Make sure your filenames match one of these patterns.

---

## Exploratory Data Analysis (EDA)

EDA was conducted to understand the structure and distribution of the data.

Steps included:

* Summary statistics (mean, std, min, max)
* Feature comparison between high and low popularity songs
* Histograms for distribution analysis
* Correlation matrices

### Key Observations

* High popularity songs tend to have higher energy and loudness
* They are generally more danceable
* They tend to have lower acousticness and instrumentalness

These observations motivated the hypothesis testing stage.

---

## Hypothesis Testing

### Research Question

Which audio features significantly differ between high-popularity and low-popularity songs?

### Hypotheses

* **H1:** High-popularity songs have higher energy and loudness

* **H2:** High-popularity songs have higher danceability (and valence if available)

* **H3:** High-popularity songs have lower acousticness and instrumentalness

* **H0:** There is no significant difference between the two groups

### Method

* Welch’s t-test was used (different sample sizes)
* P-values were calculated for each feature
* Effect sizes (Cohen’s d) were also analyzed

### Results Summary

* Significant differences were found in:

  * energy
  * loudness
  * danceability
  * acousticness
  * instrumentalness

* Some features showed weaker or no significant differences:

  * liveness
  * speechiness

### Conclusion

The results suggest that popular songs are generally:

* louder
* more energetic
* more danceable
* less acoustic and instrumental

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* SciPy

---

## Next Steps

* Apply machine learning models to predict song popularity
* Improve model performance and evaluation






