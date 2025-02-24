# Student Performance Analysis

### Project Overview

- This project aims to analyze student performance based on various factors such as gender, ethnicity, parental education, lunch type, and test preparation course. The model predicts student scores in reading, writing, and math using machine learning techniques.

### Project Structure

#### The project consists of the following components:

```plaintext
artifacts/ - Stores trained models, processed data, and hyperparameter tuning results.  
notebook/ - Contains Jupyter notebooks for data exploration and transformation.  
src/ - Houses the core implementation of the prediction pipeline.  
templates/ - Contains HTML templates for the web application.  
.gitignore - Specifies files to be ignored by Git (e.g., large datasets, logs).  
Procfile - Used for deployment, typically for platforms like Heroku.  
README.md - Documentation file for the project.  
app.py - The main Flask application handling predictions.  
requirements.txt - Lists all dependencies required to run the project.  
setup.py - Script for setting up the project as a package.  
```

### Dataset Description

- The dataset (stud.csv) contains student information with both numerical and categorical features.

- Features include:

1. Categorical: Gender, ethnicity, parental level of education, lunch type, test preparation course.

2. Numerical: Reading score, writing score, and math score (target variable).

- Data preprocessing includes checking for missing values, duplicates, and performing exploratory data analysis (EDA).

### Handling Outliers

- Outliers were identified using boxplots and statistical measures.

- Methods used to handle outliers:

1. Z-score method to detect extreme values.

2. IQR (Interquartile Range) method to filter out values outside the range of 1.5 times the IQR.



## Regression Model Used

- Several regression models were tested, including:

1. Linear Regression

2. Ridge Regression

3. Lasso Regression

4. Random Forest Regressor

5. Decision Tree Regressor

6. Support Vector Regressor (SVR)

7. KNN Regressor

8. AdaBoost Regressor

## Best Performing Model:

- The model with the highest R² score on test data was selected.

- Random Forest Regressor and Ridge Regression performed well in comparison.

**Model Selection Criteria**

- Models were evaluated using:

1. Mean Squared Error (MSE)

2. Mean Absolute Error (MAE)

3. R² Score (Coefficient of Determination)

4. Hyperparameter tuning was done using RandomizedSearchCV to optimize performance.

## Insights from Data

- Parental education level has a significant impact on student performance.

- Students who completed test preparation courses performed better.

- Lunch type (standard/reduced) also showed a correlation with performance.

- Reading and writing scores are closely related, meaning students who do well in one tend to do well in the other.

## Conclusion

- The analysis provides insights into factors influencing student performance.

- The model can help predict student scores and identify at-risk students.

- Future improvements can include deep learning models or more advanced feature engineering.

## Installation

To set up the project, follow these steps:

1. Clone the repository:
```bash
git clone https://github.com/your-repo/student-performance-analysis.git
cd student-performance-analysis
```
2.
```bash
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate
pip install -r requirements.txt
```
## Usage

#### Running the Flask App

To start the Flask application, run:
```bash
python app.py
```
- Access the web application at [http://127.0.0.1:5000/.](http://127.0.0.1:5000/.)

## Predicting Student Performance

- Enter student details in the form (gender, ethnicity, parental education, lunch, test preparation course, reading & writing scores).

- Click the "Predict" button.

- The model will predict and display the expected math score.

## Technologies Used

- Python

- Pandas, NumPy

- Scikit-learn

- Flask

- HTML, CSS

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to enhance the project.

## License

This project is licensed under the MIT License.