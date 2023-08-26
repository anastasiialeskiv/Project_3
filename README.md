### Anastasiia Leskiv

![Coronary-heart-disease](https://github.com/anastasiialeskiv/Project_3/assets/124845922/790b0f67-554e-45b5-940b-50a94e5e9d9a)

# Overview
More than 16 million people have heart disease and it’s only in the USA. About 7 percent of Americans aged 20 and older have CHD. Together with the health care organization we decided to create a classification model to predict whether or not patients have a heart disease. I used a Heart disease data set which contained thousands of data points. I built classification algorithms and then I selected the best model to present to my client. In this project I was focusing on the best accuracy of the model.

# Business and Data Understanding
More than 16 million people have heart disease and it’s only in the USA. About 7 percent of Americans aged 20 and older have CHD. Together with the health care organization we decided to create a classification model to predict whether or not patients have a heart disease. I used a Heart disease data set which contained thousands of data points. I built classification algorithms and then I selected the best model to present to my client. In this project I was focusing on the best accuracy of the model.
### Features:
Age: age of the patient [years]

Sex: sex of the patient [M: Male, F: Female]

ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]

RestingBP: resting blood pressure [mm Hg]

Cholesterol: serum cholesterol [mm/dl]

FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]

RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]

MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]

ExerciseAngina: exercise-induced angina [Y: Yes, N: No]

Oldpeak: oldpeak = ST [Numeric value measured in depression]

ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]

HeartDisease: output class [1: heart disease, 0: Normal]

![explor data](https://github.com/anastasiialeskiv/Project_3/assets/124845922/3123255a-2377-4c31-8b0e-9df8d0fade67)


Each square shows the correlation between the variables on each axis. Correlation ranges from -1 to +1. Values closer to zero means there is no linear trend between the two variables. The close to 1 the correlation is the more positively correlated they are; that is as one increases so does the other and the closer to 1 the stronger this relationship is. A correlation closer to -1 is similar, but instead of both increasing one variable will decrease as the other increases. The diagonals are all 1/dark because those squares are correlating each variable to itself (so it's a perfect correlation). For the rest the larger the number and darker the color the higher the correlation between the two variables.

![HD ](https://github.com/anastasiialeskiv/Project_3/assets/124845922/81cf4e30-b56c-423c-96a4-4ee0b0828476)

In this plot we can see that in this dataset 44.66% of people don't have Heart Disease and 55.34% of people have Heart Disease

![sex](https://github.com/anastasiialeskiv/Project_3/assets/124845922/f64cbf1b-3787-44fd-9497-9d67bb8d5252)

This plot shows that in our data set we have more males with heart disease then females.
Female Proscentage: 21.02%
Male Percentage: 78.98%

![image](https://github.com/anastasiialeskiv/Project_3/assets/124845922/07046a78-d44c-49b2-81e6-98a54c21ee61)

This plot shows us that people have heart disease at the age of 50-65 it very rarely happens to young people.

![image](https://github.com/anastasiialeskiv/Project_3/assets/124845922/1fc8943a-78f5-4c97-bc76-14d9b4a8bfc0)

If fasting Lavel of sugar more then 120 mg/dl people with heart disease almost 3 times more then without

![image](https://github.com/anastasiialeskiv/Project_3/assets/124845922/8a9ad9ee-2031-464a-b80b-1fd8deb3e418)

People with Angina defenatly have a risk to get Heart Disease


# Modeling

<img width="1047" alt="Screenshot 2023-08-17 at 8 08 03 PM" src="https://github.com/anastasiialeskiv/Project_3/assets/124845922/56d2527e-2a46-4477-bc79-f94ebf859845">


Accuracy is a measure of how well a model is able to predict the correct output for a given input. It is usually expressed as a percentage

Precision defines how accurately a model can predict the true positive rate. It's calculated as the number of true positives divided by the total number of predicted positives

Recall measures the model’s ability to classify all positive examples. It is calculated by taking the correctly identified positives, over all the actual positives in our dataset. Note the difference here from precision is that precision takes into account the predicted positives and false positives, whereas recall takes into the total number of actual positives from our dataset.

The F1 score is the harmonic mean of precision and recall. In statistics, the harmonic mean is a type of average that is calculated by taking the reciprocal of the arithmetic mean of the reciprocals of a set of numbers. It is often used to average rates or ratios, such as speeds or grades.In the context of the F1 score, the harmonic mean is used to combine the precision and recall of a classifier into a single metric. The F1 score is defined as the harmonic mean of precision and recall, with a score of 1 being the best possible score and a score of 0 being the worst. The F1 score is often used as a balance between precision and recall.


# Evaluation
![image](https://github.com/anastasiialeskiv/Project_3/assets/124845922/b8f24c8c-0d30-4ad4-b995-7d1cda3d6f11)



Score of 0.9 means the classifier can almost perfectly distinguish between all the Positive and the Negative class points.
ROC AUC score tells us how efficient the model is. The higher the AUC, the better the model's performance at distinguishing between the positive and negative classes. An AUC score of 1 means the classifier can perfectly distinguish between all the Positive and the Negative class points.



![image](https://github.com/anastasiialeskiv/Project_3/assets/124845922/3a3a7559-41d8-4cce-b65a-cf3a0c7ea01e)



True Positive(we predict our patient has Heart Disease and patient actually has it)-29

True Negative (we predict our patient does not have Heart Disease and patient actually has it)-105

False Positive(we predict our patient has Heart Disease and patient actually does not have it)-2

False Negative(we predict our patient does not have Heart Disease and patient actually has it)-48

# Conclusion
The whole dataset was aplit into 80/20 train/holdout. Prediction on 20% holdout were limited till the end.

Mens getting Heart Disease much more often the females. Also we can see that age plays a large role in the development of Heart Disease.
If fasting Lavel of sugar more then 120 mg/dl people with heart disease almost 3 times more then without

People with Angina defenatly have a risk to get Heart Disease



My model predicted with

Accuracy: 0.5978

Precision: 0.6051

Recall: 0.8879

F1: 0.7197

Where Accuracy is a measure of how well a model is able to predict the correct output for a given input. It is usually expressed as a percentage

Precision defines how accurately a model can predict the true positive rate. It's calculated as the number of true positives divided by the total number of predicted positives

Recall measures the model’s ability to classify all positive examples. It is calculated by taking the correctly identified positives, over all the actual positives in our dataset. Note the difference here from precision is that precision takes into account the predicted positives and false positives, whereas recall takes into the total number of actual positives from our dataset.

The F1 score is the harmonic mean of precision and recall. In statistics, the harmonic mean is a type of average that is calculated by taking the reciprocal of the arithmetic mean of the reciprocals of a set of numbers. It is often used to average rates or ratios, such as speeds or grades.In the context of the F1 score, the harmonic mean is used to combine the precision and recall of a classifier into a single metric. The F1 score is defined as the harmonic mean of precision and recall, with a score of 1 being the best possible score and a score of 0 being the worst. The F1 score is often used as a balance between precision and recall.

The Area under the ROC curve is 0.89 which is good score.

Overall model could be improved with more data.



## Limitation
If I would have bigger dataset I woul make better prediction.I wish I would also have more information ebout patients health information,genetics, and habbits. I would like to have some survey to see why there is bigger percentage of mans with Heart Disease, and why Age effect percentage of people with Heart Disease.

## Recommendation

I would recommend to my client to pay more attention to patient's sugar leve, blood pressure, to be more attentive to patients with age of 50 and older, and patients who experienced Angina.Also I would recommend to keep in mind that men get heart disease much more often than women.

## Next Steps
My next step would be to continue with developing model for better result. Use more data for better prediction.

├── .gitignore

├── Heart_Disease_Prediction.ipynb

├── README.md

└── archive.zip
