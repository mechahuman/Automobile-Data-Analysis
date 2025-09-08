# Data Visualization and KNNRegression

This [project](https://github.com/mechahuman/Automobile-Data-Analysis/) contains an in-depth analysis of the [Automobile dataset](https://www.kaggle.com/datasets/tawfikelmetwally/automobile-dataset ), focusing on performance metrics, efficiency trends, historical insights, and predictive modeling using machine learning.

---

## Project Overview

The purpose of this project is to analyze a dataset of automobiles produced between 1970 and 1982.  
The analysis explores relationships between attributes such as fuel efficiency, horsepower, displacement, weight, and acceleration.  
In addition to exploratory analysis, this project applies **K-Nearest Neighbors (KNN) Regression** to predict **acceleration (0–60 mph time)** based on automobile features.


---

## Dataset Description

- **Number of rows**: 398  
- **Number of columns**: 9  

**Features:**
- `name`: Car model name  
- `mpg`: Miles per gallon (fuel efficiency)  
- `cylinders`: Number of engine cylinders  
- `displacement`: Engine displacement (cubic inches)  
- `horsepower`: Engine horsepower (with missing values)  
- `weight`: Vehicle weight (lbs)  
- `acceleration`: Time to accelerate (0–60 mph) in seconds  
- `model_year`: Year of the model (1970–1982)  
- `origin`: Country of origin (USA, Europe, Japan)  

---

## Key Insights

- The average fuel efficiency (MPG) is 23.5, with values ranging from 9 to 46.6.  
- Vehicle weight shows a strong negative correlation with fuel efficiency.  
- Cars manufactured in Japan and Europe tend to be more fuel-efficient compared to those from the USA.  
- The average horsepower is 104, with significant variation across vehicles.  
- The number of cylinders is strongly associated with displacement and fuel efficiency.  

---

## KNN Regression Implementation

The dataset was used to build a **K-Nearest Neighbors (KNN) regression model** with the following steps:

1. **Data Preprocessing**
   - Missing values in the `horsepower` column were replaced with the mean value (rounded).  
   - Features (`X`) were selected: `mpg`, `cylinders`, `displacement`, `horsepower`, `weight`.  
   - The target (`y`) was set as the `acceleration` column.  
   - Data was split into training and testing sets (80% training, 20% testing).  

2. **Model Training**
   - A `KNeighborsRegressor` was trained using a user-defined number of neighbors (`k`).  
   - The model was fitted on the training data (`x_train`, `y_train`).  

3. **Model Evaluation**
   The trained model was evaluated on the test set using multiple metrics:
   - Accuracy (R² score)  : 0.6263
   - Mean Squared Error (MSE)  : 2.7579
   - Root Mean Squared Error (RMSE)  : 1.6607
   - Mean Absolute Error (MAE)  : 1.2853
   - Mean Absolute Percentage Error (MAPE)  : 8.21%
  
#### [Jupyter Notebook](https://github.com/mechahuman/Automobile-Data-Analysis/blob/main/datasetanalysis.ipynb)

These metrics provide a comprehensive understanding of model performance and its ability to predict **acceleration** from car features.

---

## Repository Structure

- `innovative.ipynb` — Jupyter Notebook containing the analysis, visualizations, and KNN regression model.  
- `Automobile.csv` — Dataset used for the analysis.  

---

## License
This project is under [MIT License](LICENSE)
