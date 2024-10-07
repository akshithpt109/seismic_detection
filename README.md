# Project: Seismic Data Analysis and Arrival Time Prediction

This repository contains all the necessary files, scripts, and data used in our project to analyze seismic data and predict the arrival time of seismic events using machine learning models. Below is a brief description of each file in the repository:

## Files and Descriptions

- **`main.ipynb`**: 
  - This is the primary notebook used to generate the final output catalog from the test seismic files. It loads the trained model, extracts features from the testing miniSEED files, and uses the model to predict the arrival times. The results are saved in the `output_catalog.csv`.

- **`Master_Features.ipynb`**:
  - A notebook used for feature experimentation and extraction from the training seismic dataset. In this notebook, we explored different features like STA/LTA, amplitude metrics, energy thresholds, and other time-domain features. The output from this analysis was used to create the `Features.csv` file.

- **`ML_Experiments.ipynb`**:
  - A notebook where we experimented with different machine learning models to determine the best model for predicting arrival times. Various models like KNN, Random Forest, Gradient Boosting, and Stacking Regressors were tested to identify the model that yields the best performance.

- **`Features.csv`**:
  - This CSV file contains the dataset with extracted features from the training data. The features include statistical, time-domain, and frequency-domain metrics used for training the machine learning models. It serves as the input for model training and evaluation in our ML experiments.

- **`output_catalog.csv`**:
  - The final output catalog generated from `main.ipynb` using the test seismic data. It includes the filenames of the seismic data and the predicted arrival times for each file. This is the file submitted as the final result of our model's predictions.

- **`knn_model.pkl`**:
  - This is the serialized KNN model file used for predicting arrival times in the `main.ipynb` notebook. It was trained using the features extracted in `Features.csv` and saved for reuse, ensuring consistent predictions during testing and submission.

- **`README.md`**:
  - This file provides an overview of the project, including explanations for each file, the purpose of the repository, and instructions for using the provided notebooks and data.

## Project Overview

The goal of this project was to develop a machine learning model capable of accurately predicting the arrival time of seismic events from miniSEED files. We achieved this by extracting meaningful features from the training data, testing various regression models, and selecting the best-performing model. The trained model was then applied to the test files given, which are documented in the `output_catalog.csv`.

