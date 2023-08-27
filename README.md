## Flu Shot Learning | Multi-label Classification

Project Description and Dataset source: https://www.drivendata.org/competitions/66/flu-shot-learning/page/210/

### Flu Shot Learning: Predict H1N1 and Seasonal Flu Vaccines

**Project Overview:**
The "Flu Shot Learning" project addresses the critical challenge of predicting whether individuals have received H1N1 and seasonal flu vaccines. By analyzing data related to backgrounds, opinions, and health behaviors, the project aims to provide insights into vaccination trends and patterns. This predictive analysis contributes to the understanding of vaccination adoption and guides public health efforts.

**Vaccination as a Public Health Measure:**
Vaccination is a cornerstone of public health, aiding in preventing the spread of infectious diseases. The project recognizes the importance of immunization and explores how it can be predicted based on various factors. Understanding individual vaccination choices is crucial for achieving herd immunity and curbing the spread of diseases.

**Historical Context:**
The project harkens back to the H1N1 influenza pandemic of 2009, also known as the "swine flu." This global pandemic led to significant morbidity and mortality. The dataset used for this project is derived from the National 2009 H1N1 Flu Survey, conducted during the early stages of the pandemic. The dataset includes information about respondents' vaccination status, demographics, opinions, and health behaviors.

**Problem Description:**
The primary goal is to predict the likelihood of individuals receiving H1N1 and seasonal flu vaccines. The prediction involves two binary target variables: h1n1_vaccine and seasonal_vaccine. Each row in the dataset corresponds to a respondent of the survey. The project involves a multilabel classification task, as respondents can receive either, both, or none of the vaccines.

**Features and Labels:**
The dataset comprises 36 columns, with features providing insights into respondents' characteristics, opinions, and health behaviors. The two target variables are:
- h1n1_vaccine: Whether the respondent received the H1N1 flu vaccine.
- seasonal_vaccine: Whether the respondent received the seasonal flu vaccine.

**Analysis and Model Creation Steps:**

1. **Feature Identification and Preprocessing:**
   - Examined the nature of features to identify their types: ordinal, categorical, numerical, or unique.
   - Addressed features with missing values by imputing them using mean or median, focusing on features with missing values below a threshold.
   
2. **Data Visualization:**
   - Utilized Seaborn for data visualization to gain insights into the relationships between features and vaccination status.
   
3. **Encoding Categorical and Ordinal Features:**
   - Transformed categorical and ordinal features into numerical representations to make them compatible with machine learning algorithms.
   
4. **Imbalance Checking:**
   - Assessed the balance of the dataset with respect to target variables to ensure a fair representation of each class.

5. **Missing Value Imputation:**
   - Employed simple imputers with mean and median values for missing value imputation.
   - Compared the distribution of original and imputed columns using density plots and box plots to validate the imputation's impact.

6. **Model Training and Selection:**
   - Explored a range of classification models, including XGBClassifier, RandomForestClassifier, DecisionTreeClassifier, KNeighborsClassifier, LogisticRegression, and SVC.
   - Applied the Label Powerset Method and Classifier Chain Method, considering the multilabel nature of the problem.
   - Conducted hyperparameter tuning using Grid Search for each model.
   - Selected "XGBoost with Classifier Chain" as the final model based on its highest AUC Score.


**Performance Metric:**
The project's performance is evaluated using the area under the receiver operating characteristic curve (ROC AUC) for each target variable (h1n1_vaccine and seasonal_vaccine). The overall score is determined as the mean of these two scores. Achieved 

AUC Score of 0.85, indicating good model performance.

**Conclusion:**
The "Flu Shot Learning" project exemplifies the application of machine learning in predicting vaccination behaviors. By analyzing data related to backgrounds, opinions, and health behaviors, the project offers valuable insights into the factors influencing flu vaccine adoption. The chosen model's accuracy and ROC AUC scores demonstrate its capability in predicting vaccination outcomes based on individual characteristics.

**Relevance and Impact:**
The project's insights are relevant to public health initiatives aimed at improving vaccine coverage. By understanding the predictors of vaccination decisions, health authorities can tailor interventions to target specific groups, enhance vaccine uptake, and contribute to disease prevention strategies.

---
