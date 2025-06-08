# Salifort Motors HR Analytics Capstone Project

## Overview

This project analyzes HR data from Salifort Motors to identify factors influencing employee attrition and to build predictive models that help the HR department proactively address employee turnover. 
The analysis includes data cleaning, exploratory data analysis (EDA), feature engineering, and the development of machine learning models to predict whether an employee will leave the company.

## Business Problem

Salifort Motors has experienced significant employee turnover, and the company seeks to understand:

- What factors contribute to employee attrition

- Predict which employees are at hight risk of leaving

## Dataset 

The dataset contains information about past and present employees, including:

- Satisfaction level
- Evaluation scores
- Average monthly hours worked
- Time at the company
- Accidents at work
- Number of projects
- Promotions in the last 5 years
- Department
- Salary

## Metodology

The project follows the PACE framework:

1. **Data Cleaning**: Standardized column names, handled missing values, and removed duplicates.
2. **EDA**: Explored relationships between satisfaction, evaluation, projects, hours, promotions, department, and salary with attrition.
3. **Feature Engineering**: Encoded categorical variables and prepared data for modeling.
4. **Modeling**: Built and evaluated logistic regression, decision tree, and random forest models.
5. **Model Evaluation**: Used metrics such as accuracy, precision, recall, F1-score, and ROC AUC to assess model performance.


## Models Built

- Logistic Regression 

- Stratified Logistic Regression 

- Decision Tree (GridSearchCV + ROC AUC tuning)

- Random Forest (GridSearchCV + ROC AUC tuning)

## Metrics Evaluated

Accuracy

Precision

Recall

F1 Score

ROC AUC

## Modeling & Evaluation

A **Random Forest** classifier (500 trees) was tuned via 5-fold CV to maximize ROC AUC.  
The plot below shows each feature’s relative importance in predicting who will leave:

![Random Forest Feature Importance](images/rf_feature_importance.png)

- **Top 3 drivers** of attrition:  
  1. **Satisfaction level**  
  2. **Average monthly hours**  
  3. **Last evaluation score**  
- **Performance on test set:**  
  - Accuracy: 98.5%  
  - Precision: 99.1%  
  - Recall: 91.6%  
  - F1 Score: 95.2%  
  - ROC AUC: 0.98  

We compared these results against the Decision Tree and Logistic Regression models using the same metrics. The Random Forest offered the best overall AUC, while the Decision Tree had the highest recall, and the Logistic Regression provided the most interpretable coefficients.


## Project Structure

- `HR_Attrition_Capstone.ipynb`: Main Jupyter notebook containing all code, analysis, and visualizations.
- `HR_capstone_dataset.csv`: The dataset used for analysis.
- `decision_tree_model.pkl`, `logistic_model.pkl`, `logistic_model_stratified.pkl`, `model_strat_balance.pkl`, `random_forest_best_model.pkl`: Saved machine learning models.
- `requirements.txt`: List of Python dependencies.
- `Salifor Autos Project.docx`: Project summary document.

## How to Run

1. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```
2. Open `HR_Attrition_Capstone.ipynb` in Jupyter Notebook or VS Code.
3. Run the notebook cells sequentially to reproduce the analysis and results.

## Results

- Identified key predictors of attrition: satisfaction level, number of projects, average monthly hours, time spent at the company, promotion history, and salary.
- The best-performing model can be used to predict which employees are at risk of leaving, enabling targeted HR interventions.

## Ethical Considerations

- Data privacy and anonymization were maintained.
- Analysis avoids introducing bias or unfair treatment based on sensitive attributes.
- Recommendations are intended to improve employee wellbeing and retention.

## Acknowledgments

This project is part of the Google Advance Data Analytics Certificate

## License

This project is for educational purposes only.

For questions or collaboration inquiries, feel free to reach out.