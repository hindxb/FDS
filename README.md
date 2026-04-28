# FDS

#Project File

# Urban Traffic Flow Prediction and Signal Optimization

## Overview
This project focuses on predicting urban traffic speeds and optimizing traffic signal timings using machine learning and spatial-temporal analysis. The goal is to improve traffic flow, reduce congestion, and enhance decision-making in smart city environments.

The system combines time-series forecasting using deep learning with a rule-based optimization framework that dynamically adjusts traffic signal timings based on predicted congestion levels.

---

## Objectives
- Predict traffic speed using historical and contextual features  
- Capture temporal patterns (time of day, day of week, trends)  
- Incorporate spatial relationships between road segments  
- Optimize traffic signal timings based on congestion priority  
- Visualize traffic conditions before and after optimization  

---

## Dataset
The dataset consists of urban traffic data including:
- Traffic speed measurements  
- Road segment information (start/end coordinates)  
- Temporal features (timestamps, day, hour)  
- Additional signals (bus count, message count, etc.)

Dataset link:  
**[https://catalog.data.gov/dataset/chicago-traffic-tracker-historical-congestion-estimates-by-segment-2024-current]**

---

## Methodology

### 1. Data Preprocessing
- Missing value handling using hybrid imputation  
- Time parsing and ordering  
- Filtering segments with sufficient historical data  

### 2. Feature Engineering
- Lag features (previous speeds)  
- Rolling statistics (mean, standard deviation)  
- Temporal encoding (sin/cos transformations)  
- Segment-level statistics  
- Speed trend features  

### 3. Prediction Model
- Model: Gated Recurrent Unit (GRU)  , LSTM, SVR, KNN, XGBoost
- Input: sequence of past traffic observations  
- Output: predicted traffic speed  

The models captures short-term temporal dependencies and traffic patterns across road segments.

---

## Signal Optimization Framework

The optimization uses predicted speeds to adjust traffic signals:

### Key Steps
1. Compute congestion score  
2. Incorporate temporal congestion (past values)  
3. Add spatial congestion (neighboring roads)  
4. Calculate priority score  
5. Allocate green signal time dynamically  

### Key Equation
Congestion Score:

C = 1 - (Predicted Speed / Max Reference Speed)

Priority Score:

P = 0.70 × Temporal Congestion + 0.30 × Neighbor Congestion

---

## Visualization
- Interactive traffic maps using Folium  
- Color-coded congestion levels  
- Side-by-side comparison:
  - Before optimization  
  - After optimization  

---

## Results
- Improved traffic speeds after optimization  
- Better allocation of green signal time  
- Reduction in congestion in high-priority segments  

---

## Technologies Used
- Python  
- Pandas, NumPy  
- TensorFlow / Keras  
- Scikit-learn  
- Folium (map visualization)  
- ipywidgets (interactive controls)  

---

## Notes
- Interactive components (widgets) may not render on GitHub  
- For full interactivity, run the notebook in Google Colab  

---

## Future Work
- Integrate real-time traffic data  
- Improve optimization using reinforcement learning  
- Extend to multi-intersection coordination  
- Incorporate external factors (weather, events)  










----------------------------------------------------------------------------------------------------------------
#Class Activity File

Foundation of Data Science Course

This folder contains the midterm assessment of the foundation of datascience course in the university of shrajah. The idea is to learn how to read, understand and manipulate datasets using tables in the datascience library.

The Iris dataset is one of the most well-known datasets in data science. It contains measurements of 150 iris flowers across 3 species: setosa, versicolor, and virginica. You can download or open Iris dataset using https://www.kaggle.com/datasets/uciml/iris 

The datascience library lets you read the table, calculate means, and add predictions to the table. In addition, the project assist in learning how to visualize scatter plots and create the model line to predict petal width values from petal length to understand the relationships between the two values.

to access the colab file, you may click on: https://colab.research.google.com/github/hindxb/FDS/blob/main/Notebooks/Class%20Activities/Hind_Alzarooni_MA.ipynb

Done by: Hind Alzarooni
ID: U25102248
University: University of Sharjah
