# Unmasking Rating Inflation in Atlanta’s Restaurants

## Team
Honglai Peng, Qinyang Song, Xiaoran Zhu, Duanduan Zhou, Xin He

## Introduction

In the bustling culinary landscape of Atlanta, the phenomenon of "Rating Inflation" has emerged as a significant concern. Characterized by an upward trend in average ratings coupled with a diminishing variance, this phenomenon not only obscures the true quality of dining experiences but also misguides potential customers. Our research delves into the underlying causes of Rating Inflation, with a keen focus on overlooked aspects such as review recency and the detection of fake reviews.

## Motivation & Objectives

The cornerstone of our study is the understanding that while previous research has laid a solid foundation on the mechanics and biases of online ratings, the granular analysis of rating data itself remains paramount. Our endeavor aims to:

- Illuminate the mechanisms behind Rating Inflation in online restaurant reviews.
- Introduce novel methodologies to emphasize review recency and enhance fake reviews detection.

## Data Overview

Our analysis leverages a refined subset of Google Local Data, meticulously curated to include 1,327 restaurants across Atlanta, encapsulating over 760,525 reviews post filtration. In response to the absence of pre-trained models adept at identifying fake reviews, we've also compiled a balanced dataset comprising over 56,000 entries, evenly distributed between authentic and deceptive reviews.

## Methodological Approaches

### Time Decay Recency Adjustment

Our innovative recency adjustment technique marries time-decay modeling with Bayesian averaging to recalibrate the influence of reviews over time. This approach not only diminishes the weight of older reviews but also amplifies the significance of recent feedback, thereby fostering a more dynamic and accurate representation of a restaurant's current standing.

### Dual-stage Fake Reviews Removal

Employing a synergistic blend of CNN-LSTM and BERT models, our strategy aims to meticulously sift through reviews, isolating genuine feedback from the chaff of deception. This dual-stage process ensures a robust defense against the misleading impacts of fabricated reviews.

## Data Visualization & Interactive Exploration

Through a comprehensive recalibration of the rating system and an insightful spatial distribution analysis, we unveil the tangible impacts of fake reviews. Our interactive maps and multifaceted charts serve as a testament to the efficacy of our approaches, offering a vivid depiction of the rating landscape pre and post-intervention.

## Conclusion & Future Directions

Our investigation into Rating Inflation within Atlanta's restaurant scene not only enhances the accuracy and reliability of customer feedback but also sheds light on the imperative need for advanced fake review detection mechanisms. As we look towards the future, the integration of sentiment analysis looms on the horizon, promising a more nuanced and insightful exploration of customer feedback.

Join us in navigating the intricate web of ratings, as we strive to bring truth and clarity to the forefront of the online review ecosystem.




# InflateDeflate-RatingsAnalysis Setup Guide

This repository provides detailed setup instructions for sessions 1, 2, 3, and 4, encompassing data preparation, Google Colab configuration, and troubleshooting tips.

## Google Drive Preparation

Create a `CSE6242` folder in your Google Drive and upload the following datasets and files:

### Data Preprocessing:
- `meta-Georgia.json`
- `review-Georgia.json`

### Recency Adjustment:
- `complete_file_merged_filtered.csv`

### Fake Reviews Removal:
- `combined_reviews.csv`
- `updated_filtered_atlanta_restaurant_reviews.csv`

### Data Analysis:
- `updated_filtered_atlanta_restaurant_reviews.csv`
- `complete_file_merged_filtered_adjusted_1125.csv`
- `complete_file_merged_filtered.csv`

## Google Colab Configuration

- Sign in with your Google account.
- Enable GPU runtime: `Runtime > Change runtime type > Select GPU`.

## Troubleshooting

- Ensure GPU support is enabled.
- Verify dataset file names and paths.
- Adjust batch sizes or dataset sizes for memory issues.

## Detailed Steps

### 1. Data Pre-processing

- Mount Google Drive in "DataPreprocessing.ipynb".
- Load `meta-Georgia.json` and `review-Georgia.json`.
- Generate "filtered_atlanta_restaurant_reviews.csv" through preprocessing.

### 2. Recency Adjustment

- Mount Google Drive in "RecencyAdjustment.ipynb".
- Adjust data based on recency from 'complete_file_merged_filtered.csv'.

### 3. Fake Reviews Removal

- Setup and install libraries in "FakeDetectionBert.ipynb".
- Train BERT and CNN-LSTM models for fake reviews detection.

### 4. Data Analysis and Visualization

- Load and analyze data in "DataAnalysis_1.ipynb" and "DataAnalysis_2.ipynb".
- Generate visualizations as detailed in the report.

### 5. Interactive Map Setup

- Install the latest version of Node.js.
- Run `npm install` and `npm start` to launch the application.
- Visit http://localhost:3000 in your browser.

## Directory Overview

### Images

Contains screenshots demonstrating the web page.

### Data-preprocess

Includes a notebook for data processing after fake reviews removal and recency adjustment.

### Public

Stores setup files and preprocessed data csv files.

### Src

Contains all visualization code and components for the web app.

## Video Demo

Watch our interactive map demonstration on [YouTube](https://youtu.be/iyEandlyeTE?si=WgcSlC5iPHhnJ20V).


