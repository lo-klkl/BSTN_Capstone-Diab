# Detecting Bias in Hospital Admissions in Diabetic Patients 
Kristen L
_____
#### Purpose: 

I aim to leverage machine learning models to evaluate the likelihood of hospital admission of diabetic patients given their prior medical history, current complaints, and demographic data. My primary objective is to shed light on the glaring issue of healthcare inequity at a systemic level. The first step in fixing a problem is acknowledging that there is one. 

I plan to create a discrimination test to evaluate if the raw data being fed into the models contains biased information which could worsen or create new forms of disparities, removing this biased information, and then using that data for modeling.  But first, I'd like to be able to create models that do not undergo testing so that I can benchmark what basic performance looks like. Further research is still required for me to be able to implement the discrimination test as a part of my pipeline. 

By harnessing the power of data, I aspire to ensure that every patient has the opportunity for the best possible outcome.

Ideally, we would be following the pipeline as set out by [Raza](https://www.sciencedirect.com/science/article/pii/S2772442522000430) as shown here:

![image](https://ars.els-cdn.com/content/image/1-s2.0-S2772442522000430-gr1.jpg)
_____
#### Information about Data: 
- [Data Dictionary](Docs/DataDictionary.pdf): This contains the data dictionary for the final clean data set that was used for analysis.
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
    - The purpose of this notebook is to do a baseline Exploratory Data Analysis (EDA) to understand the data that lives within the columns and their relationship to the target column. Some feature engineering will be done as we analyze the `Chief Complaint` and `Prior Medical History` columns. After performing a phi-coefficient score with their respective p-values, those that do not meet the 0.05 threshold will be removed from the dataset. See EDA results [here](Docs/EDA_Results.md).
- [Notebook #3: Pre-processing](Notebooks/Pt2-Preprocessing.ipynb): 
    - The purpose of this notebook is to pre-process the data and ready it for modeling. In the end, all of the columns will be binary and dummy columns will be created. [Here](Docs/Dummy_Ref.md) is a guide to understanding the dummy columns that were dropped to avoid multicollinearity and to be used as a reference.
- [Notebook #4: Modelling - Pt1](Notebooks/Pt3-Modelling-Pt1.ipynb):
    - The purpose of this notebook is to develop simple base models while also doing some feature engineering/elimination as well. The two baseline models being made and optimized are Logistic regression and Decision Tree.
    - The models can be found here: [Logisit Regression](Models/KLO_BStn_LogReg.joblib) and [Decision Tree](Models/KLO_BStn_DTree.joblib)
- [Notebook #5: Modelling - Pt2](Notebooks/Pt3-Modelling-Pt1.ipynb):
    - The purpose of this notebook is the develop advanced models, I have chosen to do Random Forest and xGBoost as it's the most appropriate given the binary nature of my dataset.
    - The models can be found here: [Random Forest](Models/KLO_BStn_RF.joblib) and [xGBoost](Models/KLO_BStn_xGB.json)

______
#### Future Plans:
      
- Model deployment:
    - I plan to eventually make a web app where users can input their own demographic data and the model will be able to return the likelihood of hospital admission just solely on demographic data.

- Further research into how to implement IBM's aif360 library in preprocessing to ensure that all data going into the model is unbiased then gauging its effect on accuracy. If the loss in accuracy is negligible, then it shouldn't be an issue to implement this as a part of pre-processing.
  
______
#### Data resource

Courtesy of:
 "Hong WS, Haimovich AD, Taylor RA (2018) Predicting hospital admission at emergency department triage using machine learning. PLoS ONE 13(7): e0201016." (https://doi.org/10.1371/journal.pone.0201016)

 The dataset is also available on [github here](https://github.com/yaleemmlc/admissionprediction)

[Raza, S. (2022)“A Machine Learning Model for Predicting, Diagnosing, and Mitigating Health Disparities in Hospital Readmission.” Healthcare Analytics, Elsevier](https://www.sciencedirect.com/science/article/pii/S2772442522000430)
______
#### Other files
- [Sprint 1 project presentation](Docs/KristenLo_Sprint1_Presentation.pdf)
- [Sprint 2 project presentation](Docs/KristenLo_Sprint2_Presentation.pdf)
- [Sprint 3 protect presentation](Docs/KristenLo_Sprint3_Presentation.pdf)

