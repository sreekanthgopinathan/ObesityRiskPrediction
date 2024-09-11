### Captstone : Obesity Risk Prediction
**Sreekanth Gopinathan (@sreekanth.gopinathan@gmail.com)**

#### Executive summary

Cardiovascular disease (CVD) mortality and morbidity has been shown to be elevated in individuals who are overweight. Goal of the study is to use various factors to predict obesity risk in individuals, which is related to cardiovascular disease. 

#### Rationale (Source : https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3250069/)

Obesity is among the leading causes of elevated cardiovascular disease (CVD) mortality and morbidity. Overweight and obesity are defined by the World Health Organization as abnormal or excessive fat that accumulate and present a risk to health.1 Obesity is measured in body mass index (BMI), which is a person’s weight (in kilograms) divided by the square of his or her height (in meters). A person with a BMI of 30 or more is generally considered obese. A person with a BMI equal to or more than 25 is considered overweight.1,2

The degree and incidence of obesity in the U.S. has been increasing in both adults and children.3 In the United States, nearly 70% of adults are classified as overweight or obese.3 An estimate of 2.6 million deaths worldwide and 2.3% of the global burden of disease are caused by obesity.4,5 Obesity was found to be a major risk factor for the development of type-2 diabetes, asthma, hypertension, stroke, coronary artery disease, cancer and cancer-related mortality, liver and gallbladder diseases, sleep apnea, osteoarthritis, and gynecological complications.2,6 Obesity also adds to risk once the levels of coexisting risk factors are taken into account. Obesity is associated with elevated blood pressure, blood lipids, and blood glucose; changes in body weight are coincident with changes in these risk factors for disease.7,8

Cardiovascular disease (CVD) mortality and morbidity has been shown to be elevated in individuals who are overweight, particularly with central deposition of adipose tissues.4 Abdominal obesity has been shown to be a risk factor for CVD worldwide

#### Research Question

The objectives of this study are: 
* Understand the relationship between various features that increases obesity risk in individuals, which is related to cardiovascular disease
* Build and evaluate multiple classficication models to predict predict obesity risk in individuals
* Provide actionable insights to improve effectiveness of future health programs/initiatives to proactively identify obesity risk in population and take actiosn to mitigate the risks

#### Data Sources
The dataset was generated from a deep learning model trained on the Obesity or CVD risk dataset. 
Kaggle Source : https://www.kaggle.com/competitions/playground-series-s4e2/overview

#### Methodology

*  Understanding the Data
   * Descriptive statistics to  understand data distribution
   * Visualizations to understand relationships & correlations between features  
*  Feature Engineering
   * Handling any missing values, duplicates & outliers
   * Encode any categorical & ordinal values
   * Normalize and scale any features
*  Select model & evaluate
   *   Begin with a base model
   *   Use performance metrics to evaluate (accuracy, precision, recall, F1-score, AUC) and determine the metric to optimize
   *   Use classification algorithms :  Logistic Regression, KNN ,Decision Tree, and Support Vector Machines to build the predictive model.
   *   Hyperparameter Tuning: Grid search and cross-validation to optimize model performance.
*  Feature Importance Analysis
   * Identify features based on their contribution to the predictive model

#### Results
So far the project has completed the Exploratory Data Analysis (EDA) with a Initial baseline model that is able to predict outcome with a accuracy score of 96%

#### Next steps
Complete the remaining phases of the project (model selection & evaluation and feature importance analysis)

#### Outline of project

Link to the Colab Project : https://colab.research.google.com/drive/1LVPG5EW6_rQHEdUzpRTmc5sGfAC-uCjX?usp=sharing
Link to github project : https://github.com/sreekanthgopinathan/ObesityRiskPrediction

##### Contact and Further Information# ObesityRiskPrediction
