# Detecting Bias in Hospital Admissions
Kristen L

#### Purpose: 

I aim to leverage machine learning models to evaluate the likelihood of hospital admission based on an individual's medical history and demographic data. My primary objective is to shed light on the glaring issue of healthcare inequity at a systemic level. The first step in fixing a problem is acknowledging that there is one. The primary aim of this project is to identify if any biases exist in the healthcare outcome of patients based on demographic data while accounting for past medical history and reason for visits to the ER. By harnessing the power of data, I aspire to ensure that every patient has the opportunity for the best possible outcome.

#### Information about Data: 
- [Data Dictionary](Docs/Data_Dictionary_for_Capstone-Final.pdf): This contains the data dictionary for the final clean data set that was used for analysis.
- [Categorizing Numeric columns guide](Docs/categorizing_col_guide): This contains the guide used to convert numerical to categorical columns to provide context.
- [Prelim EDA results](Docs/PrelimEDA_Results.md): This contains the resutls from the preliminary EDA done on the data. Mostly looking into distribution and geneneral effect on outcome.

#### Creating the environment 
- Follow the guide in the requirements [here](Docs/requirements.txt)

#### Notebooks

###### [Notebook #1: Part 0 Data cleaning](Notebooks/Pt0-Clean.ipynb) 
(Table of Contents in the notebook)
- Part 0: Cleaning the Data
    - 1.1: Housekeeping
    - 1.2: Deleting Columns
    - 1.3: Deleting Rows
    - 1.4: Handling Duplicates
    - 1.5: Data Type Conversion
    - 1.6: Handling Missing Data
    - 1.7: Categorizing Columns
- Conclusion

###### [Notebook #2: Preliminary EDA (In Progress)](Notebooks/Pt1-PrelimEDA.ipynb)
(Table of Contents in the notebook)
- Part 1: Preliminary EDA
    - 1.1: Housekeeping
    - 1.2: Disposition vs Demographic
    - 1.3: Disposition vs Triage Categorical Variables
    - 1.4: Disposition vs Triage Numerical Variables
    - 1.5: Disposition vs Hospital Usage
    - 1.6: Disposition vs Chief Complaint
    - 1.7: Disposition vs Prior Medical History
    - 1.8: Miscellaneous Insights
- Conclusion

### Completed:
- Cleaning the data (see clean notebook for more details) 
- Changing numerical columns to categorical columns to make interpretation and EDA easier and also setting up for dummying these columns down the road. 
- Prelim EDA, understanding the data in the columns, how columns relate to the target, and their significance in relation to the target. 
        See Prelim EDA results [here](Docs/PrelimEDA_Results.md)
  
#### Current status:
- The plan is to dig further into the relationships between the unique categorical column entries and the target (admittance). For instance, how does being white/caucasian affect the admittance rate? This will also live in the Prelim EDA notebook under 1.8 Miscellaneous Insights so that I don't need to start another notebook.
- To accomplish this, the various categorical columns would need to be dummied, which is good as preparation for modeling to complete one-hot encoding. I plan to drop the column with the most instances as this would be the reference column for all of my dummy columns.
  

### Future Plans: 
- Feature selection and Dimensionality reduction. After dummying the categorical columns, I anticipate the total columns to be about 600-700. This is necessary so that the most relevant features can be kept and the less informative ones discarded. This will help with improving model performance, reducing overfitting, and speeding up the training process.
    -  I plan to start with Recursive Feature Elimination (RFE) to perform an initial feature selection and reduce the feature space to a manageable size.
    -  I was already going to use a logistic model as my base model. Applying L1 regularization within a logistic regression model to further refine the feature set and promote sparsity in the coefficients. This can help select the most informative features while also allowing for easy interpretation.
      
- Modelling:
    - The baseline model that I plan to use is a logistic regression. I plan to also use this with the Lasso regularization to see how I can base optimize my model
    - I plan to also try other models to see which performs the best:
      - Random forest: Random Forest can handle datasets with a large number of features, making it a good choice for so many binary features. It can capture complex relationships between features and the target variable. Random Forest provides feature importance scores, which can help identify which binary features are the most informative.
      - Gradient Boosting (xGBoost): an ensemble technique that builds decision trees sequentially, with each tree correcting the errors of the previous one. Gradient Boosting models are known for their high predictive power. Can also be used for feature importance scores. Regularization techniques can also be used to prevent overfitting.
      - Support Vector Machines (SVM): great choice for binary classification and can be used in high-dimensional data sets with many features.
    - After seeing which model runs the best, I will then make sure to check for various hyperparameters to further optimize the model.
    - Make sure to evaluate the model's accuracy, precision, recall, F1-score, and area under the ROC curve (AUC-ROC).
      
- Model deployment:
    - I plan to eventually make a web app where users can input their own demographic data and the model will be able to return the likelihood of hospital admission just solely on demographic data. 

#### Data resource

Courtesy of:
 "Hong WS, Haimovich AD, Taylor RA (2018) Predicting hospital admission at emergency department triage using machine learning. PLoS ONE 13(7): e0201016." (https://doi.org/10.1371/journal.pone.0201016)

 The dataset is also available on [github here](https://github.com/yaleemmlc/admissionprediction)

#### Other files
- [Sprint 1 project presentation](Docs/KristenLo_Sprint1_Presentation.pdf)
- [Sprint 2 project presentation](Docs/KristenLo_Sprint2_Presentation.pdf)

