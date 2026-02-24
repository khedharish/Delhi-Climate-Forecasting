# Delhi Climate Forecasting using Deep Learning

## Overview
This project implements a deep learning–based time-series forecasting system to predict daily climate trends in Delhi using historical weather data. Two different sequence models — an LSTM and a Transformer — are trained independently, and their predictions are combined using an ensemble approach to improve robustness and forecasting accuracy.


---

## Problem Statement
Accurate climate forecasting plays a key role in urban planning, agriculture, and energy management.  
The goal of this project is to model historical climate data and forecast future temperature values by learning temporal dependencies using deep learning techniques.

---

## Dataset
- **Dataset:** Daily Delhi Climate Dataset  
- **Train Set:** Historical climate data used for model training  
- **Test Set:** Held-out data used for evaluation  

Files:
- `DailyDelhiClimateTrain.csv`
- `DailyDelhiClimateTest.csv`

## Approach

### 1. Data Preprocessing
- Selected relevant climate variables from the dataset  
- Applied MinMax normalization to scale values consistently  
- Converted time-series data into fixed-length input sequences using a sliding window approach  

### 2. Model Architectures

**LSTM Model**
- Captures sequential dependencies in climate time-series data  
- Effective for learning long-term temporal trends  

**Transformer Model**
- Utilizes self-attention mechanisms to capture global temporal relationships  
- Handles long-range dependencies more efficiently than traditional RNN-based models  

### 3. Ensemble Strategy
- Generated predictions independently from both LSTM and Transformer models  
- Combined outputs using an ensemble approach  
- Reduced individual model bias and improved overall forecast stability  
- Final predictions represent aggregated outputs from both models  

### 4. Evaluation
- Evaluated models on unseen test data  
- Compared predicted values against actual observations  
- Visualized performance trends to assess temporal alignment  

---

## Results
- Both LSTM and Transformer models successfully capture seasonal temperature patterns  
- The ensemble model produces smoother and more stable predictions compared to individual models  
- Training convergence is stable, as observed from loss curves  