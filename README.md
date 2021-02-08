TITLE : 
Project Report on Fetal Health dataset using various classifier models.

INTRODUCTION : 
In this project, I have built various model of the ‘Fetal Health Classification’ dataset which contains various information of the fetus. Fetal mortality is a public health issue that put in risk the women’s or baby’s life. This project uses several Machine Learning Classification techniques in order to predict the risk level of the fetal health, it attempts to classify that into three classes namely-
1.	Normal
2.	Suspect
3.	Pathological
Cardiotocography (CTG) is used during pregnancy to monitor fetal heart rate and uterine contractions. It is monitor fetal well-being and allows early detection of fetal distress. CTG interpretation helps in determining if the pregnancy is high or low risk. In this project, I created models to classify the outcome of Cardiotocogram test to ensure the well-being of the fetus.

DATASET EXPLORATION : 
The foremost step to begin with the journey of analysis of data is to explore the data then various analysis and visualization methods and information acquisition will be done with Python. This dataset was explored using various inbuilt function like info (), shape (), unique () to know the variable/ column names, values and observations in the dataset. This gave us a quick insight into the dataset. Accessing the column names gave a quick idea as from where the analysis should be start.

Columns: 
•	baseline value - Baseline Fetal Heart Rate (FHR)
•	accelerations - Number of accelerations per second
•	fetal movement - Number of fetal movements per second
•	uterine contractions - Number of uterine contractions per second
•	light decelerations - Number of LDs per second
•	severe decelerations - Number of SDs per second
•	prolongued decelerations - Number of PDs per second
•	abnormal short-term variability - Percentage of time with abnormal short-term variability
•	mean value of short-term variability - Mean value of short-term variability
•	percentage of time with abnormal long-term variability - Percentage of time with abnormal long-term variability
•	Hear beat counts details – The mean, median, mode, minimum, maximum, number of peaks, number of zeroes, variance and tendency.
•	Fetal Health – Classified into three classes- Normal, Suspect and Pathological.

DATA ANALYSIS :
After exploring the dataset, there was a need to analyze the data. In this study, I aimed to find a correlation between Fetal Health and different factors, and compare them. I found that baseline value followed by decelerations and abnormal long-term variability have a high correlation with Fetal Health indicating they are major factors in predicting the Fetal Health.

Y AND X VARIABLE FRAMEWORK : 
In this dataset, my Y variable was Fetal Health and the X variables were baseline value, accelerations, fetal movement, uterine contractions, light decelerations, severe decelerations, prolongued decelerations, abnormal short-term variability, mean value of short-term variability, percentage of time with abnormal long-term variability, Heart Beat Counts details.

DATA PRE-PROCESSING : 
Handling Missing Values: - There are no null values in the dataset.	
Encoding the categorical Variables: - In this dataset, there is one categorical variable ---Fetal Health (Normal, Suspect and Pathological). As it is a Y variable so doing label encoding using the map function is the best way. 

DATA VISUALIZATION : 
Data Visualization is the most important step because it gives the visual summary of the data which makes it easier for a layman as well to understand and identify the data patterns and trends than looking through thousands of rows on a spreadsheet. 
So, to gain insights, we have visualized our Fetal Health prediction dataset using various visualization methods. In this project, we have used various graphs like bar plot, boxplot, violin plot, histogram and heatmap to give a clear picture of the dataset.

By analysing all the plots created in the project code, we can see that,
•	More than 70% fetal health is normal which is a good sign that fetus is healthy enough.
•	Baseline Value seems to hold some correlation to Fetal Health.
•	There seems to be a strong positive correlation between Decelerations and Fetal Health.
•	There is a very strong relationship between the histogram mean, median and the mode of the fetus heartbeat.
•	By looking at the box plot, we can say that Baseline Fetal Heart rate for Suspect class is having maximum value followed by the other classes.

Correlation: From the heatmap, we can see that, Decelerations has the highest impact on the Fetal health, even though the Fetal Health is affected by abnormal long-term variability, baseline value, histogram variance. Other variables didn’t show a strong correlation with the Fetal Health(y) variable.

STANDARDIZATION : 
As, in this dataset, there are different ranges of values, which can deviate our results. So, scaling is required to avoid that situation.  I used StandardScaler which is a class of sklearn.

K-FOLD CROSS VALIDATION SCORE : 
The k-fold cross-validation procedure is a standard method for estimating the performance of a machine learning algorithms or configurations on a dataset. 
The motivation to use cross validation techniques is that when we fit a model, we are fitting it to a training dataset. Without cross validation we only have information on how does our model perform to our in-sample data. Ideally, we would like to see how does the model perform when we have a new data in terms of accuracy of its predictions. 

SPLITTING THE DATA INTO TRAIN AND TEST AND MODEL CREATION : 
After splitting the data into Training and Testing, model building was done. There are many models for machine learning, and each model has its own strengths and weaknesses. In this project, I have tried various classification algorithms and tuned the parameters using the GridSearchCV which tries all the combinations of the values passed in the dictionary and evaluates the model for each combination using the Cross-Validation method. Hence after using this function we get accuracy/loss for every combination of hyperparameters and we can choose the one with the best performance.

The classifiers I used to find the best model out of them are: -
1)	Logistic Regression
2)	K-Nearest Neighbors (KNN) Classifier
3)	Support Vector Machine (SVM)
4)	Decision Tree Classifier
5)	Random Forest Classifier
6)	AdaBoost Classifier

FINAL CONCLUSION : 
After comparing all the six models, I came to this conclusion which will help to choose the best model out of all the models to get the best results.
•	Out of all the models, Random Forest Classifier and the AdaBoost Classifier showed the best scores.
•	Test scores for all the models are near to the Best Scores.
•	K-Fold Cross Validation scores are a bit higher in Random Forest Classifier Model.
•	It seems to be that AdaBoost Classifier with 95% accuracy and the Random Forest Classifier with 94% accuracy are the best performing models.
•	As per the Classification Report, maximum predictions were caught correctly in Random Forest Classifier and the AdaBoost Classifier.
•	The test and the training scores for the Logistic Regression and the Support Vector Classifier are near to each other resulting them as the best fit models whereas others showed some sort of overfitting.

So, as per other scores Random Forest Classifier and the AdaBoost Classifier are the best performing models but the best fit models are the Logistic Regression and the Support Vector Classifier model.
