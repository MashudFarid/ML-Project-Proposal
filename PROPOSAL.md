# ML Project Proposal
- Mashud Fariduddin S/0 Mohammad Yusoff
- Top 2018 

## What track are you choosing (analysis or engineering)?
Analysis 

## What is your data source?
https://mavenanalytics.io/data-playground

## Summarize the status of your data and what cleaning is needed.
Summary of Dataset Status:
- Size: 100 rows and 16 columns.
- Data Types:

   - Object columns:
id, name, artists (all non-null)

- Numeric columns:
   - 13 numeric columns (float64): danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo, duration_ms, time_signature.
     
- Non-Null Values:
  - All columns are fully populated with no missing values.

- Potential Cleaning Tasks:
1. Check for Duplicates (e.g., based on id or name).
2. Outlier Detection for numeric values (e.g., extreme values in loudness, tempo).
3. Format Consistency:
 -  Ensure consistent capitalization and remove any leading/trailing spaces in name and artists.
4. Data Type Adjustments:
 - Columns like key, mode, and time_signature could potentially be integers instead of floats.

Suggested Data Cleaning Step 

1. Check for Duplicates:
- Ensure that there are no duplicate rows based on the id or song names.

2. Outlier Detection:
- Review the numeric columns for potential outliers or values outside expected ranges (e.g., loudness or tempo).

3. Consistency Checks:
- Ensure consistent formatting in name and artists columns (e.g., no leading/trailing spaces, uniform casing).

4. Data Type Verification:
- The key, mode, time_signature columns might be better represented as integers.

## Summarize the structure of your data and what models/techniques work with it.
The dataset contains 100 records of songs with various features. The structure can be broken down into two main types: categorical (object) and numerical (float64) columns.

1. Categorical Data:
- id: Unique identifier for each song.
- name: Song title.
- artists: Artist(s) performing the song.
2. Numerical Data (Float Columns):
- Audio Features (continuous values):
  - danceability: How suitable the track is for dancing (range 0 to 1).
  - energy: Intensity and activity of the track (range 0 to 1).
  - loudness: Overall loudness in decibels (negative values, closer to 0 are louder).
  - speechiness: Speech-like quality in the track (range 0 to 1).
  - acousticness: Likelihood of being acoustic (range 0 to 1).
  - instrumentalness: Degree of instrumental content (range 0 to 1).
  - liveness: Presence of a live audience (range 0 to 1).
  - valence: Positivity of the track (range 0 to 1).
  - tempo: Beats per minute.
    
- Other Numeric Attributes:
  - key: Musical key (may range from 0 to 11, corresponding to musical notes).
  - mode: Whether the song is in a major or minor key (0 or 1).
  - duration_ms: Song duration in milliseconds.
  - time_signature: Time signature of the track (usually 4).

Potential Models to Use:
Depending on the goal of your analysis, here are some model suggestions:

1. Regression:
If you're trying to predict a continuous variable like tempo, loudness, or duration_ms, regression models are suitable:
- Linear Regression
- Decision Trees or Random Forests
- Gradient Boosting

2. Classification:
If you want to classify songs based on categories such as mode (major/minor) or key, then classification models are appropriate:
- Logistic Regression
- Support Vector Machines (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest Classifier

3. Clustering:
For unsupervised grouping of songs based on similar audio features:
- K-Means Clustering
- Hierarchical Clustering

5. Dimensionality Reduction (for visualization):
If you want to visualize similarities or differences in songs:
- Principal Component Analysis (PCA)
- t-SNE


## What is your overall goal with this project?
To find the top artist of 2018 

## Anything else you want to note about your project?
NIL
