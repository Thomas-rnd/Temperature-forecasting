# Exploring Long-Term Temperature Forecasts: CNNs to Attention-Enhanced ConvLSTMs

## Abstract

This repository contains the implementation and findings of our research project, "Temperature Forecasting with Deep Learning." We explore the application of deep neural networks in weather forecasting, with a focus on predicting the 2m temperature over South Korea for the next 24 months. The project compares traditional Numerical Weather Prediction (NWP) models with data-driven neural network models, including a Convolutional Neural Network (CNN), ConvLSTM (recurrent neural network with convolutional filters), and an attention-enriched ConvLSTM.

## 1. Introduction

Weather forecasting is crucial for various sectors, impacting agriculture, energy, tourism, and more. This paper focuses on predicting temperature changes in South Korea, emphasizing the importance of local forecasts. It explores the use of deep neural networks, contrasting them with traditional NWP models and highlighting the potential of data-driven approaches in Earth science applications.

## 2. Methods

### 2.1 Dataset

Meteorological data from the ERA5 Reanalysis dataset was used, covering hourly estimates of climate variables from 1940 to the present. Data variables were collected over South Korea at five evenly separated dates each month.

### 2.2 Data Handling and Data Reduction Techniques

Eight features were selected based on an Exhaustive Feature Search (EFS), and the dataset was split into training, validation, and testing sets. Monthly averages were computed for each coordinate, creating a supervised time series dataset.

![Data preprocessing](https://github.com/Thomas-rnd/temperature_forecasting/blob/main/images/5ddata_image.jpg)

### 2.3 Model Architectures

Three models were explored:

#### 2.3.1 Convolutional Neural Network (CNN)

A simple CNN with one layer and 32 channels was trained using Mean Squared Error as the loss function.

#### 2.3.2 ConvLSTM

The ConvLSTM model combines convolutional operations for spatial features and a gated LSTM for temporal coherence, generating a 2-year forecast.

#### 2.3.3 ConvLSTM with Attention

This model incorporates a ProbSparse Attention Layer to enhance spatial-temporal data analysis, dynamically adjusting feature weighting for improved predictive accuracy.

## 3. Results and Analysis

View the results and analysis in the [Final_Report.pdf](https://github.com/Thomas-rnd/temperature_forecasting/blob/main/Final_Report.pdf) file.

![Results](https://github.com/Thomas-rnd/temperature_forecasting/blob/main/images/temperatures_forecast_CNN-LSTM_Pohang-si.png)

## 4. Conclusion

Our findings suggest that ConvLSTM models offer efficiency and effectiveness in weather forecasting, reducing inference time compared to traditional NWP methods. The ConvLSTM model proves to be an efficient approach for understanding and predicting climatic trends over extended periods, showcasing its potential for widespread application and decision support.
