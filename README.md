# Student Performance Analytics

A comprehensive data science project analyzing student performance in secondary education using the UCI Machine Learning Repository Student Performance dataset.

## Project Overview

This project investigates how student data (attendance, grades, demographic, social, and school-related attributes) can be analyzed to improve learning outcomes. The research focuses on:

- Identifying dropout risks
- Analyzing course engagement
- Enabling personalized learning interventions

## Dataset

The project uses the **Student Performance Data Set** from the UCI Machine Learning Repository, which includes data from two Portuguese secondary schools covering Mathematics and Portuguese language courses.

**Dataset Source:** [UCI Machine Learning Repository - Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance)

**Features:** 33 attributes including demographic information, socio-economic factors, school-related data, and grades (G1, G2, G3).

## Project Structure

```
student-performance-analytics/
├── student-mat.csv                    # Mathematics course data
├── student-por.csv                    # Portuguese course data
├── combined_student_performance.csv   # Combined dataset
├── preprocessed_student_performance.csv # Preprocessed data
├── X_test.csv                         # Test features
├── y_test.csv                         # Test target
├── create_boxplots.py                 # Script for generating visualizations
├── g3_distribution.png                # Final grade distribution
├── correlation_heatmap.png            # Feature correlation heatmap
├── categorical_g3_boxplots.png        # Box plots for categorical features
├── linear_regression.pkl              # Trained Linear Regression model
├── random_forest_regressor.pkl        # Trained Random Forest model
├── gradient_boosting_regressor.pkl    # Trained Gradient Boosting model
├── model_evaluation_results.csv       # Model performance metrics
├── problem_statement.md               # Problem definition and objectives
├── data_description.md                # Dataset description
├── methodology_implementation.md      # Methodology details
├── statistical_analysis_evaluation.md # Statistical analysis and evaluation
└── README.md                          # This file
```

## Methodology

1. **Data Preprocessing:** Cleaned and combined Mathematics and Portuguese datasets, applied one-hot encoding to categorical variables, and converted binary features to numerical format.

2. **Exploratory Data Analysis:** Conducted comprehensive EDA including distribution analysis, correlation studies, and categorical feature comparisons.

3. **Model Building:** Implemented three regression models:
   - Linear Regression (baseline)
   - Random Forest Regressor
   - Gradient Boosting Regressor

4. **Evaluation:** Assessed models using MAE, MSE, RMSE, and R² metrics.

## Key Findings

- **Best Model:** Gradient Boosting Regressor achieved the best performance with MAE of 2.50, RMSE of 3.39, and R² of 0.26.
- **Important Factors:** Parental education, study time, past failures, and absences significantly influence student performance.
- **Subject Differences:** Portuguese language students show slightly higher and more consistent performance compared to Mathematics students.

## Model Performance

| Model                       | MAE  | MSE   | RMSE | R²   |
| :-------------------------- | :--- | :---- | :--- | :--- |
| Linear Regression           | 2.62 | 13.63 | 3.69 | 0.12 |
| Random Forest Regressor     | 2.53 | 11.93 | 3.45 | 0.23 |
| Gradient Boosting Regressor | 2.50 | 11.50 | 3.39 | 0.26 |

## Requirements

```
Python 3.11+
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

## Installation

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

## Usage

1. **Run EDA visualizations:**
   ```bash
   python3.11 create_boxplots.py
   ```

2. **Load and use trained models:**
   ```python
   import joblib
   model = joblib.load('gradient_boosting_regressor.pkl')
   predictions = model.predict(X_test)
   ```

## Innovation & Applications

- **Interactive Dashboard:** Web-based visualization tool for educators and administrators
- **Early Warning System API:** Integration with school management systems for real-time risk assessment
- **Personalized Learning Recommendations:** Data-driven intervention suggestions based on student profiles

## References

1. P. Cortez and A. Silva. Using Data Mining to Predict Secondary School Student Performance. In A. Brito and J. Teixeira Eds., Proceedings of 5th FUture BUsiness TEChnology Conference (FUBUTEC 2008) pp. 5-12, Porto, Portugal, April, 2008, EUROSIS, ISBN 978-9077381-39-7.
2. UCI Machine Learning Repository: [https://archive.ics.uci.edu/dataset/320/student+performance](https://archive.ics.uci.edu/dataset/320/student+performance)

## License

This project uses the Student Performance dataset licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).

## Author

**Excellent Andile**

## Acknowledgments

- Paulo Cortez and A. M. G. Silva for the original dataset
- UCI Machine Learning Repository for hosting the dataset
