# California House Price Prediction Model
![image](https://github.com/user-attachments/assets/01baea68-8691-479d-9fb9-f8be22b121d9)

This project aims to predict housing prices using California housing data. It involves data preprocessing, feature engineering, and applying machine learning models such as Linear Regression and Random Forest Regressor to achieve a robust prediction.

---

## Project Overview

**This project uses:**
+ Python and libraries like pandas, numpy, matplotlib, and seaborn for data analysis and visualization.
+ scikit-learn for preprocessing, splitting datasets, and applying machine learning algorithms.
+ The primary goal is to predict median house values based on various features like location, room count, and income.

> [!TIP]
> Open the `HousePricePrediction.ipynb` for more details regarding results and visualization of data.

---

## Dataset
The dataset for this project includes the following features:
- `longitude` and `latitude` (location data)  
- `housing_median_age`  
- `total_rooms`, `total_bedrooms`  
- `population`, `households`  
- `median_income`  
- `median_house_value` (target variable)  
- `ocean_proximity` (categorical feature)  

> [!IMPORTANT]
> This was made possible using the [California Housing Prices Dataset](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

---

## **Project Workflow**
### 1. **Data Loading and Cleaning**
- Imported the dataset using `pandas`.
- Checked for missing values and dropped rows with null values in the `total_bedrooms` column.

### 2. **Data Preprocessing**
- Applied logarithmic transformation to skewed columns like `total_rooms`, `total_bedrooms`, `population`, and `households` to normalize distributions.
- Created new features:
  - `bedroom_ratio` = `total_bedrooms / total_rooms`
  - `household_rooms` = `total_rooms / households`
- Encoded the categorical feature `ocean_proximity` using one-hot encoding.

### 3. **Data Visualization**
- Used **histograms** to analyze feature distributions.  
- Correlation heatmaps (`sns.heatmap`) to understand relationships between features.  
- Scatter plots to analyze the effect of `latitude` and `longitude` on `median_house_value`.

### 4. **Model Training**
- **Linear Regression** and **Random Forest Regressor** were applied:
   - `StandardScaler` was used to standardize numerical features.  
   - Random Forest achieved a performance score of **0.82** on the test data.
 
---

## **Code Structure**
- **`housing.csv`**: Input dataset file.  
- **`main.py`**: Python script with the full workflow.  
- **`README.md`**: Project documentation.
  
---

## **Key Results**
- Random Forest Regressor achieved an **R² score of 0.82**, indicating strong performance for housing price prediction.  
- Log transformations and feature engineering significantly improved model accuracy.

---
## **Libraries Used**
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
---

## **How to Run the Code**
1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/housing-price-prediction.git
   cd housing-price-prediction
2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
3. Run the script:
   ```bash
   python main.py

---

## **Future Improvements**
- Test additional machine learning models like XGBoost or LightGBM.
- Use cross-validation to fine-tune hyperparameters.
- Explore more advanced feature engineering techniques

---

## Author
- **Fied Elahresh**
- View personal website or profile README for contact details
