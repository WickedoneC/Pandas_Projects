# Diabetes Prediction Using Health Indicators

Dataset taken from Kaggle: https://archive.ics.uci.edu/ml/datasets/Early+stage+diabetes+risk+prediction+dataset

Models used:
-K-Means Clustering
-Decision Tree
-KNN
-Log Reg
-SVM
-Naive Bayes

Evaluation:
-f1_score assuming all positive - .76
-dummy classifier respecting sample dist - .60
-dummy classifier picking at random - .51

-K-Means Clustering - .86 <br/>
-Decision Tree - .94 <br/>
-KNN - .99 <br/>
-Log Reg - .94 <br/>
-SVM - .98 <br/>
-Naive Bayes - .94 <br/>

GridSearch was used in combination with cross validation to find the optimal parameters and fit to the training set. 

K-Means clustering gave a high f1 score, implying the two classes are clearly distinguishable.

All models worked well, producing scores of over 90. This could be due to the small size of the dataset or the significance of each feature. KNN and SVM both worked particularly well, both models creating boundaries to separate the classes. 

Looking at feature importance with the Decistion Tree, it's clear that the presence of polyuria is a significant indicator relative to the other features. Age, gender, and the presence of polydipsia were also important features. 

The f1 score was used to evaluate the models. However, when looking at the problem, it's more important to maintain high recall in the model and minimize the false negative rate (people diagnosed as healthy when they actually have diabetes).


