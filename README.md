# Fashion Recommendation System using CNN

## Project Description

This project aims to recommend the top 5 similar images from a dataset based on an input image. The system involves data cleaning, visualization, CNN-based feature extraction, and a recommendation system to find image similarities using extracted features.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Usage](#usage)
- [Methods](#methods)
- [Results](#results)
- [Contributing](#contributing)

## Introduction

In the fashion industry, finding similar items based on an image is a common requirement. This project uses Convolutional Neural Networks (CNN) to extract features from images and recommend similar items from a dataset. The project is implemented in Python using popular libraries such as pandas, matplotlib, and TensorFlow/Keras.

## Dataset

The dataset used in this project includes images of various clothing items and their corresponding metadata. The dataset is loaded and cleaned to handle missing values and irrelevant information.

## Usage

1. Load and clean the dataset:
   ```python
   import pandas as pd
   df = pd.read_csv("styles.csv")
   # Additional data cleaning steps
   ```

2. Visualize the data:
   ```python
   import matplotlib.pyplot as plt
   df["gender"].value_counts().plot(kind="pie", autopct='%1.2f%%', explode=[0.1]*5)
   ```

3. Extract features using CNN:
   ```python
   from keras.models import load_model
   model = load_model("your_cnn_model.pkl")
   # Feature extraction code
   ```

4. Get recommendations:
   ```python
   similar_images = get_similar_images(input_image, model, dataset)
   # Function to find and display similar images
   ```

## Methods

### Data Loading and Cleaning

- Loading datasets using pandas.
- Checking and handling missing values.
- Dropping unnecessary data.

### Data Visualization

- Using matplotlib for visualizing the distribution of categories.

### Feature Extraction

- Implementing CNN for feature extraction from images.

### Recommendation System

- Calculating similarities between images using extracted features.
- Recommending top 5 similar images.

## Results

The system successfully recommends the top 5 similar images based on the input image. The similarity is calculated using features extracted by the CNN model.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.
