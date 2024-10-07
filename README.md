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

#### Data Analysis
* Dataset includes 20758 entries. Some of the key features incuded in the dataset include :
  * General features
    * Gender,
    * Age,
    * Height
    * Weight

  * Features  related with eating habits
    * FAVC : Frequent consumption of high caloric food,
    * FCVC : Frequency of consumption of vegetables,
    * NCP : Number of main meals,
    * CAEC : Consumption of food between meals,
    * CH20 Consumption of water daily, and
    * CALC : Consumption of alcohol

  * Features  related with the physical condition
    * SCC : Calories consumption monitoring,
    * FAF : Physical activity frequency,
    * TUE : Time using technology devices
    * MTRANS : Transportation used

  * Target variable is 
    * Underweight Less than 18.5
    * Normal_Weight 18.5 to 24.9
    * Overweight 25.0 to 29.9
    * Obesity I 30.0 to 34.9
    * Overweight_Level_II 35.0 to 39.9
    * Obesity III Higher than 40

  * For simplfying the analysis, converted target variable to a binary classification of 0 for outcomes Obesity I, II and III and 0 otherwise


* Weight appears to be a clear predictor of obsesity. Inorder to understand other predictors, decided to drop weight from the model

<img src=./images/pairplot.png width="500" height="200">

* No major multicolinearity between independent features in the dataset validated using VIF analysis
* Dataset is observed to be balanced between the 2 binary outcome catgories 48 %  Obesity I, II and III  and 52% remaining


#### Modelling & Performance
In this project, employed various classification modeling techniques to predict success of the predicting obesity. The models evaluated include Logistical Regression, K Nearest Neighbor, Decision Tree and Support Vector machine. Each model was trained and evaluated using a train/test split. Initial results of the modelling performance as below - metrics considered include time to train, accuracy on trraining and testing data. After the initial analysis, an ensemble model, Random Forest was added. Based on initial analysis, SVM models seem to give highest accuracy but took more time than the other models

<img src=./images/initcompare.png width="500" height="200">

After adding Random Forest, the ensemble model was the clear winner in terms of accuracy

<img src=./images/finalcompare.png width="500" height="200">

After selecting the randomforest model, performed cross-validation and hyperparameter tuning using GridSearchCV to optimize performance. The best performing parameters were : Best Random Forest model score : 0.909415 using {'max_depth': None, 'n_estimators': 500}

<img src=./images/modelperformance.png width="600" height="400">

#### Conclusion

Based on the model the top 10 features which influence the model performance includes

<img src=./images/permutationimportance.png width="600" height="400">

#### Key Reccomendations

* Family history appears to be highest predictor obesity
* Age appears to be the next major predictor for obsesity
* Both Family history and age likely influences other factors such as eating habits, level of physical excercise which may result increased predictability using these factors
* Eating habits such as Consumption of food between meals,Frequency of consumption of vegetables are other major factors which predict obesity
* Overall family history, age and eating habits are a much stronger predictor of obesity compared to physical condition/attributes

#### Next Steps

Few areas for further exploration 

*   Explore possibility of breaking down factors such as family history and age into more actionable features. Features in the analysis does not correlate with family history or age which indicates there are potentially other granular features it can be broken down into
*  Device health & nutritional programs which takes into account the predictive features highlighted by the model to help reduce the incidence of  obesity

#### Outline of project

Link to the Colab Project : https://colab.research.google.com/drive/1LVPG5EW6_rQHEdUzpRTmc5sGfAC-uCjX?usp=sharing
Link to github project : https://github.com/sreekanthgopinathan/ObesityRiskPrediction

##### Contact and Further Information# ObesityRiskPrediction
