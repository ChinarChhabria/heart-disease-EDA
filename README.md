## EDA on Uci ml Dataset

### libraries used
1. pandas 🐼
3. numpy 🔢
4. seaborn 🐬 for plotting
5. matplotlib (I couldn't find an emoji for it) for visualization

### Data Description 
The data here has around 303 rows and 13 columns. We are predicting if the patient has heart disease or not.Out of the 12 feature rows 8 are categorical and rest 4 are numerical.

### Features and their explanations:
1. chol means cholestrol levels of the person 
2. fbs — fasting blood sugar > 120 mg/dl. 1 = true, 0 = false. Indicates diabetes risk.
3. restecg — resting ECG results. 0=normal, 1=ST-T wave abnormality, 2=left ventricular hypertrophy.
4. thalach — maximum heart rate achieved during stress test. Lower max heart rate can indicate heart problems.
5. cp (chest pain type) — 4 categories: 1=typical angina, 2=atypical angina, 3=non-anginal pain, 4=asymptomatic. these are different types of chest pain each shows something different
6. exang - exercise induced angina means does the person feel chest pain during or after exercise
7. oldpeak — ST depression induced by exercise relative to rest. Higher values indicate more stress on the heart.
8. slope — slope of peak exercise ST segment. 1=upsloping, 2=flat, 3=downsloping.
9. ca — number of major vessels (0-3) colored by fluoroscopy. More blocked vessels = higher disease severity. Has missing values.
10. thal — thalassemia blood disorder. 3=normal, 6=fixed defect, 7=reversible defect. Has missing values.
11. num (target) — 0 = no heart disease, 1-4 = presence of heart disease with increasing severity
12. The column trestbps means the resting blood pressure of the person when admitted to the hospital

### Observations from the data: 
1. The data consists of 68% males and 32 % females
2. The data is mostly of people from the age of 40 to 70 where the mean age is 54.
3. In the training data there are 164 people who don't have heart disease and 139 who do.

### Most important features
1. thal        
2. ca          
3. exang       
4. oldpeak     
5. thalach     
6. cp

### Visualizations: 
1. Here I plot the most important features according to correlation along with the target

### Conclusion and future improvements 
Here I have done the whole EDA along with the plots but i can add more visualizations and even read more graphs to learn more exciting things from the data. The correlation is only based on linear correlation and i can show cross correlation of the features and i can also add more visualizations.

## Model training and pipeline 
Here i used sklearn libraries to first scale the features and then i used three different types of models of logistic regression,XGboost and random forest and compared their results as it is a health disease we need recall to be more as we want to catch as much of 1 values as possible. As logistic regression had high recall scores i chose that model. Then i did error analysis and the model had a hard time predicting exceptions from the data as that is understandable even doctors are sometimes perplexed when strange symptoms come forward.

## How can i improve the model more 
I can do more error analysis and find out ways to improve the model, I could use cross validation and then get the best from random forest and xgboost and then compare to get better recall scores. 

