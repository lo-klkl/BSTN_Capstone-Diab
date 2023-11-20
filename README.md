# Detecting Bias in Hospital Admissions
Kristen L
_____
#### Purpose: 

I aim to leverage machine learning models to evaluate the likelihood of hospital admission of diabetic patients My primary objective is to shed light on the glaring issue of healthcare inequity at a systemic level. The first step in fixing a problem is acknowledging that there is one. I plan to create a discrimination test to evaluate if the raw data being fed into the models contains biased information which could worsen or create new forms of disparities, removing this biased information, and then using that data for modeling. 

By harnessing the power of data, I aspire to ensure that every patient has the opportunity for the best possible outcome.
_____
#### Information about Data: 
- [Data Dictionary](Docs/Data_Dictionary_for_Capstone-Final.pdf): This contains the data dictionary for the final clean data set that was used for analysis.
- [Categorizing Numeric columns guide](Docs/categorizing_col_guide.md): This contains the guide used to convert numerical to categorical columns to provide context.
- [EDA results](Docs/EDA_Results.md): This contains the results from the EDA done on the data. Mostly looking into distribution and the general effect on the outcome.
_____
#### Creating the environment 
- Follow the guide in the requirements [here](Docs/requirements.txt) to create the appropriate environment as well as install all necessary libraries. 
_____
#### Notebooks
- [Notebook #1: Part 0 Data cleaning](Notebooks/Pt0-Clean.ipynb) 
    - The purpose of this notebook is to sort, clean, and create a clean CSV file to do further analysis and modeling on. 
- [Notebook #2: EDA](Notebooks/Pt1-EDA.ipynb): 
    - The purpose of this notebook is to do a baseline Exploratory Data Analysis (EDA) to understand the data that lives within the columns and their relationship to the target column. Some feature engineering will be done as we analyze the `Chief Complaint` and `Prior Medical History` columns. After performing a phi-coefficient score with their respective p-values, those that do not meet the 0.05 threshold will be removed from the dataset. 
- [Notebook #3: Pre-processing](Notebooks/Pt2-Preprocessing.ipynb): 
    - The purpose of this notebook is to pre-process the data and ready it for modeling. In the end, all of the columns will be binary and dummy columns will be created. [Here](Docs/Dummy_Ref.md) is a guide to understanding the dummy columns that were dropped to avoid multicollinearity and to be used as a reference. 
______
### Completed:
- Cleaning the data (see clean notebook for more details) 
- Changing numerical columns to categorical columns to make interpretation and EDA easier and also setting up for dummying these columns down the road. 
- Exploratory Data Analysis (EDA), understanding the data in the columns, how columns relate to the target, and their significance in relation to the target. 
        See EDA results [here](Docs/EDA_Results.md)
______
#### Current status:
- Feature selection and Dimensionality reduction. This is necessary to keep the most relevant features and the least informative ones discarded. This will help with improving model performance, reducing overfitting, and speeding up the training process.
    -  I plan to start with Recursive Feature Elimination (RFE) to perform an initial feature selection and reduce the feature space to a manageable size.
    -  I was already going to use a logistic model as my base model. Applying L1 regularization within a logistic regression model to further refine the feature set and promote sparsity in the coefficients. This can help select the most informative features while also allowing for easy interpretation.
      
- Modelling:
    - The baseline model that I plan to use is a logistic regression. I plan to also use this with the Lasso regularization to see how I can base optimize my model
    - I plan to also try other models to see which performs the best:
      - Random forest: Random Forest can handle datasets with many features, making it a good choice for so many binary features. It can capture complex relationships between features and the target variable. Random Forest provides feature importance scores, which can help identify which binary features are the most informative.
      - Gradient Boosting (xGBoost): an ensemble technique that builds decision trees sequentially, with each tree correcting the errors of the previous one. Gradient Boosting models are known for their high predictive power. Can also be used for feature importance scores. Regularization techniques can also be used to prevent overfitting.
      - Support Vector Machines (SVM): great choice for binary classification and can be used in high-dimensional data sets with many features.
    - After seeing which model runs the best, I will then make sure to check for various hyperparameters to further optimize the model.
    - Make sure to evaluate the model's accuracy, precision, recall, F1-score, and area under the ROC curve (AUC-ROC).
      
- Model deployment:
    - I plan to eventually make a web app where users can input their own demographic data and the model will be able to return the likelihood of hospital admission just solely on demographic data. 
______
#### Data resource

Courtesy of:
 "Hong WS, Haimovich AD, Taylor RA (2018) Predicting hospital admission at emergency department triage using machine learning. PLoS ONE 13(7): e0201016." (https://doi.org/10.1371/journal.pone.0201016)

 The dataset is also available on [github here](https://github.com/yaleemmlc/admissionprediction)

Raza, S. (2022)“A Machine Learning Model for Predicting, Diagnosing, and Mitigating Health Disparities in Hospital Readmission.” Healthcare Analytics, Elsevier, (www.sciencedirect.com/science/article/pii/S2772442522000430)
______
#### Other files
- [Sprint 1 project presentation](Docs/KristenLo_Sprint1_Presentation.pdf)
- [Sprint 2 project presentation](Docs/KristenLo_Sprint2_Presentation.pdf)

