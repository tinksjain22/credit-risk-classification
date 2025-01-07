# credit-risk-classification


### Module 20 Report  
#### Analysis  

**Purpose of the Analysis**  
The objective of this analysis was to examine various features within the dataset and develop a predictive model to classify loans as either high-risk or healthy. The dataset used included the following features: `loan_size`, `interest_rate`, `borrower_income`, `debt_to_income`, `num_of_accounts`, `derogatory_marks`, and `total_debt`. The target variable, `loan_status`, indicated whether a loan was healthy (0) or high-risk (1).  

**Stages of the Machine Learning Process**  

1. **Target and Feature Separation**:  
   - The target variable, `loan_status`, was extracted and stored as a series (`y`), while the remaining features were stored in a DataFrame (`X`).  

2. **Data Splitting**:  
   - The dataset was divided into training and test sets using `train_test_split` from sklearn, with a random state of 1 for reproducibility.  

3. **Model Training**:  
   - A Logistic Regression model from sklearn was initialized with a random state of 1. The training data was fitted to the model.  

4. **Model Prediction**:  
   - The trained model was used to make predictions on the test data.  

5. **Performance Evaluation**:  
   - A classification report from sklearn was generated to assess the model's accuracy, precision, and recall. The metrics were calculated by comparing the predictions to the actual test target values (`y_test`).  

The results are discussed in detail in the following section.  

---

#### Results  

**Logistic Regression Model Performance:**  

- **For healthy loans (0)**:  
  - Accuracy: 92%  
  - Recall: 99%  
  - Precision: 100%  

- **For high-risk loans (1)**:  
  - Accuracy: 97%  
  - Recall: 94%  
  - Precision: 84%  

---

#### Summary  

In this analysis, a Logistic Regression model was implemented to predict loan statuses. While the model performed reasonably well, particularly in avoiding false positives for healthy loans, it misclassified 37 out of 619 high-risk loans as healthy. This represents an error rate of 6%, which may not be acceptable for financial institutions, as such misclassifications could pose significant risks.  

Overall, while the model demonstrated fair performance, it is recommended to explore additional models and techniques to improve prediction accuracy before adopting this model in a real-world scenario.
