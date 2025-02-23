# CaliforniaHousingEDA_10211100286

## Overview
This project analyzes housing prices in California using machine learning models such as Random Forest, Decision Tree, and Support Vector Machine (SVM). The goal is to:
1. Predict house prices based on available features.
2. Explore the impact of location (latitude, longitude, ocean proximity) on prices.
3. Analyze socioeconomic factors, particularly how median income and population density influence house prices.

## Dataset
The dataset used is California Housing Data, stored as `california_Housing.csv`. It contains housing-related information such as location, number of rooms, population, and median income. The dataset is cleaned and preprocessed before training machine learning models.

### Data Dictionary
| Column Name        | Data Type | Description |
|--------------------|-----------|-------------|
| `longitude`       | float     | Longitude of the block in California |
| `latitude`        | float     | Latitude of the block in California |
| `housing_median_age` | float  | Median age of the houses in the block |
| `total_rooms`     | int       | Total number of rooms in the block |
| `total_bedrooms`  | float     | Total number of bedrooms in the block (some missing values) |
| `population`      | int       | Total population in the block |
| `households`      | int       | Total number of households in the block |
| `median_income`   | float     | Median household income of residents in the block (in tens of thousands) |
| `ocean_proximity` | category  | Proximity of the block to the ocean (e.g., `NEAR BAY`, `INLAND`, etc.) |
| `median_house_value` | float  | Median house price in the block (target variable) |

## Implementation Steps
1. Data Preprocessing
   - Handle missing values by removing rows with `NaN` values.
   - Normalize numerical features using StandardScaler.
   - Encode categorical variables (e.g., `ocean_proximity`) using OneHotEncoder.
2. Model Training
   - Train three machine learning models: Random Forest, Decision Tree, and SVM.
   - Use a Pipeline to preprocess data and fit models.
   - Split the dataset into 80% training and 20% testing.
3. Model Evaluation
   - Evaluate models using Mean Squared Error (MSE) and R² Score.
   - Print performance metrics for each model.
4. Data Visualization
   - Scatter plot: Relationship between `median_income` and `median_house_value`.
   - Box plot: Impact of `ocean_proximity` on `median_house_value`.

## Results & Insights
- Higher median income correlates strongly with higher house prices.
- Houses near the ocean tend to be more expensive than inland properties.
- Random Forest outperforms Decision Tree and SVM in prediction accuracy.

## Usage Instructions
1. Ensure `california_Housing.csv` is in the same directory as the notebook.
2. Install dependencies:
   ```bash
   pip install pandas numpy seaborn scikit-learn matplotlib
   ```
3. Run the Jupyter Notebook file:
   ```bash
   jupyter notebook California_Housing_Analysis.ipynb
   ```

## Author
[Your Name] - Data Science Enthusiast

