# Bestsellers Analysis Project

## Overview

This project analyzes a dataset of bestselling books, exploring their attributes such as user ratings, reviews, price, year, and genre. The analysis includes data cleaning, exploratory data analysis (EDA), and predictive modeling to understand factors influencing book ratings and genres. The project uses Python with libraries like Pandas, Scikit-learn, and others to perform data processing and machine learning tasks.

## Dataset

The dataset, `bestsellers with categories.csv`, contains information about bestselling books from 2009 to 2019. It includes the following columns:

- **Name**: Title of the book
- **Author**: Author of the book
- **User Rating**: Average user rating (out of 5)
- **Reviews**: Number of reviews
- **Price**: Book price
- **Year**: Year of bestseller ranking
- **Genre**: Fiction or Non-Fiction

## Project Structure

- **MA_541_project.ipynb**: Jupyter Notebook containing the complete analysis, including data loading, cleaning, EDA, and modeling.
- **bestsellers with categories.csv**: The dataset used for analysis (not included in the repository; provide your own or use a similar dataset).
- **README.md**: This file, providing an overview of the project.

## Requirements

To run the notebook, install the required Python libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Analysis Workflow

1. **Data Loading**:

   - The dataset is loaded using Pandas from `bestsellers with categories.csv`.
   - A preview of the data is displayed to understand its structure.

2. **Data Cleaning**:

   - Checked for missing values (none found).
   - Checked for duplicate rows (none found).

3. **Exploratory Data Analysis (EDA)**:

   - Summary statistics for numerical columns (`User Rating`, `Reviews`, `Price`, `Year`) are generated to understand distributions.
   - Key insights:
     - Average user rating: \~4.62
     - Price range: $0 to $105
     - Reviews range: 37 to 87,841
     - Years: 2009–2019

4. **Predictive Modeling**:

   - **Regression Analysis**: Predicting `User Rating` using features like `Reviews`, `Price`, and `Year`.
     - Models tested: Linear Regression, Random Forest (initial and tuned).
     - Results:
       - Linear Regression: R² = 0.0104, MAE = 0.1737 (poor fit)
       - Random Forest (Initial): R² = 0.3246, MAE = 0.1372
       - Random Forest (Tuned): R² = 0.4459, MAE = 0.1181 (best fit, 45% variance explained)
   - **Classification Analysis**: Predicting `Genre` (Fiction vs. Non-Fiction).
     - Models tested: Logistic Regression, Random Forest Classifier.
     - Results:
       - Logistic Regression: Accuracy = 0.70 (baseline)
       - Random Forest Classifier: Accuracy = 0.8818 (best performing)

## Results

- **Regression**: The tuned Random Forest model performed best, explaining 44.59% of the variance in user ratings with an MAE of 0.1181.
- **Classification**: The Random Forest Classifier achieved the highest accuracy (88.18%) in predicting book genres.
- The analysis suggests that non-linear models like Random Forest are more effective for this dataset due to complex relationships between features.

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/bestsellers-analysis.git
   ```
2. Place the `bestsellers with categories.csv` file in the project directory.
3. Open the Jupyter Notebook:

   ```bash
   jupyter notebook MA 541 project.ipynb
   ```
4. Run all cells to reproduce the analysis.

## Future Improvements

- Incorporate additional features (e.g., book length, publication date) to improve model performance.
- Experiment with other algorithms (e.g., Gradient Boosting, Neural Networks).
- Perform feature engineering, such as text analysis of book titles or author popularity.
- Visualize relationships between variables using plots (e.g., scatter plots, histograms).

## 

## 
