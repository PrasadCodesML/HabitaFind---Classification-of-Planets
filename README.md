# HabitaFind : Classification of Planets 
This was a Hackathon by IIT Bhu - Yuri's Night (Astronomy Club)

In this Hackathon a complex dataset was given and our task was to classify the planets based on the 112 features given in the dataset
This Problem was solved using a very unique and innovative approach by combining **PCA (Principal component Analysis)** and **GridSearchCV** 

1. The all the categorical features was converted into numerical features
2. The features containing way too many classes was dropped and then rest were converted into numbers using **LabelEncoding**
3. Then the data was normalized using **MinMaxScaler**
4. Then using **SmoteTomek** Classification Bais was removed
5. And then Using **SVM** and **RF** -> SVM performed better
6. Considering SVM a loop of **PCA** and **GridSearchCV** was developed which gave the only important factors for the best accuracy
7. Finally, 0.999581764951903 of accuracy as achieved

Some questions asked at the Hackathon

1. How did you tackled categorical columns?
   Answer : There were 4048 rows and some categorical columns contained approximately 2000 or some even contained 3000 categories this may have confused the model even more so in such case removing such categorical columsn is preferable

2. How did you handled Classification Bais?
   Answer : Using SmoteTomek fake but similar classes were created of that category which contained less category and brought to the same number as rest of the classes

3. Why wasn't Deep Learning Approaches used for training the classifier?
   Answer : Since we are getting a very good accuracy just by using this simple Supervised Machine Learning approaches, there is no need to use any complex architecture for solving the things which are getting solved by such simple methods
