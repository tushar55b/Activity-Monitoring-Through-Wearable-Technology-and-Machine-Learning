# Activity Monitoring Through Wearable Technology and Machine Learning

## Introduction

This repository contains the code and documentation for the final project of Group 23 for the course Applied Machine Learning (COMS W4995 - Topics in Computer Science). The project focuses on exploring human physiological responses using wearable technology data and machine learning techniques.

The primary objective is to predict human activities based on physiological parameters such as heart rate and body temperature. The project utilizes the PAMAP2 Dataset, a comprehensive dataset capturing various physical activities performed by individuals. By applying machine learning and deep learning models, the project aims to make accurate predictions on these activities, which can have implications in health monitoring, fitness tracking, and beyond.

## Data

The dataset used in this project is the PAMAP2 Physical Activity Monitoring Dataset, collected through wireless Inertial Measurement Units and heart rate monitoring. It comprises data from 9 participants engaging in 13 distinct activities, offering a diverse set of samples for analysis.

## Methods

### Initial Data Exploration

The initial exploration reveals a large dataset consisting of over 2.8 million entries distributed across 33 columns. The dataset maintains a high temporal resolution, with entries recorded at intervals of 0.01 seconds. The primary target variable, 'activityID,' is categorical, representing 13 different activities. Data preprocessing involves encoding categorical variables and ensuring the dataset's numerical consistency.

### Data Cleaning

Minimal data cleaning is required, with only a small portion of missing heart rate data. These missing values are handled by dropping corresponding samples to maintain data integrity. Additionally, feature correlation analysis indicates no significant collinearity, ensuring the dataset's suitability for model training.

### Data Sampling

To address class imbalance, undersampling is applied to the 'transient activities' category, fostering a more equitable distribution among activity labels and improving model generalization.

## Results

### Model Selections

Two models are selected for activity prediction: K-Nearest Neighbors (KNN) and a Sequential Neural Network.

#### KNN Model

- **Training:** The KNN algorithm is trained with varying numbers of neighbors, with accuracy consistently above 93% across different configurations.
- **Evaluation:** Analysis of accuracy scores demonstrates high performance across the range of neighbor values.

#### Neural Network

- **Training:** The Sequential Neural Network, designed for multi-class classification, achieves a validation accuracy of 79.7%.
- **Evaluation:** The model exhibits competitive performance with a test accuracy of 79.7%.

## Conclusion

The project highlights the effectiveness of both KNN and Sequential Neural Network models in predicting human activities based on physiological data. While KNN excels in simplicity and transparency with high accuracy, the Sequential Neural Network demonstrates the ability to discern complex patterns, making it suitable for capturing intricate data relationships. Leveraging machine learning and deep learning techniques, the project contributes to advancements in health monitoring and fitness tracking through wearable technologies.

## Discussion

The experimentation phase also explored ensemble models such as pruned decision trees, random forests, and XGBoost. However, computational challenges arose due to the dataset's size, necessitating prolonged training times. Future work could involve exploring Long Short-Term Memory Recurrent Neural Networks (LSTM RNN) for enhanced time-series forecasting capabilities.

## Reference

[PAMAP2 Physical Activity Monitoring Dataset](https://archive.ics.uci.edu/ml/datasets/PAMAP2+Physical+Activity+Monitoring)
