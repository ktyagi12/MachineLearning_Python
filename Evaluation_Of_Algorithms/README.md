# CRITICAL ASPECT: EVALUATION OF CLASSIFIERS

**PROGRAMMING LANGUAGE USED:** Python 3.x

**IDE:** Jupyter

**AIM:**  To evaluate the performance of classifier using either ROC Curve, Accuracy measure, Recall, Precision measure, etc.

**TASKS:**

Dataset Used: HotelRevHelpfulness, BreastCancer

1. Load the dataset
2. Normalise the data
3. Build the classifier.
4. Train the model (Guassian, Multinomial, Bernoulli)
4. Predict the target class for an unknown query.
5. Evaluate the performance of the classifier.
6. Draw confusion matrix, plot ROC Curve.
7. Calculate F1 Score, Precision, Recall values of the classifiers.

**Evaluation:** Evaluating the machine learning algorithm is an essential part of any project. 
Model may give satisfying results when evaluated using a metric say accuracy_score but may give poor results when evaluated against other metrics such as logarithmic_loss or any other such metric.

**Confusion Matrix:** Confusion Matrix: It is defined as a table used to describe the performance of the model. It allows visualization of the algorithm’s performance. It consists both Predicted as well as Actual classes.

![image](https://user-images.githubusercontent.com/38240162/72688401-ccc83b00-3afe-11ea-9a49-595efbf53f7e.png)

**True Positive (TP):** A true positive is an outcome where the model correctly predicts the positive class. Observation is positive, and is predicted to be positive also.

**False Positive (FP):** A false positive is an outcome where the model incorrectly predicts the positive class. Observation is negative, but is predicted positive.

**True Negative (TN):** A true negative is an outcome where the model correctly predicts the negative class. Observation is negative, and is predicted to be negative.

**False Negative (FN):** A false negative is an outcome where the model incorrectly predicts the negative class. Observation is positive, but is predicted negative.

**Precision:** It defines what proportion of all the predictions that we made with the model are actually true. It is calculated as the ratio of correct positive predictions to the total predicted positive.

**Recall/True Positive Rate:** It is a measure that gives the fraction of all relevant documents that are successfully retrieved. It is calculated as the ratio of correct positive predictions to the total positive examples.

**F1 Measure:** It is a way of collaborating both Precision and Recall measures of any model with the help of Harmonic Mean of both of them. For uneven class distribution, where accuracy is not an apt measure, F1 measure works there. Higher the value of F1 measure, higher accuracy for the system (mostly).

**False Positive Rate:** The false positive rate is an accuracy metric, calculated as the ratio between the number of negative events wrongly categorized as positive (false positives) and the total number of actual negative events regardless of classification. The false positive rate infers to the expectancy of the false positive ratio.

**ROC Curve:** A receiver operating characteristic curve, ROC curve, is a technique widely used in machine learning to evaluate the classifier’s performance. It condenses the classifier’s performance graphically and allow us to compare the performances of various classifiers. It is a graphical plot that depicts the ability of a binary classifier system as its similarity threshold is varied. It plots the True Positive Rate against the False Positive Rate for every threshold value between 0 and 1.

**Area under ROC Curve:** To compare the classifiers, Area under Curve (AUC) is useful to summarize the performance of the classifiers in a single measure. Higher the area under curve, model is better at predicting 0s as 0 and 1s as 1. Each point on the ROC curve shows a sensitivity/specificity (TPR,FPR) pair corresponding to a similarity threshold. AUC is a metric of how well a parameter can differentiate between two classes (election/non-election). ROC Curve is shown below with equal scaling on both X and Y axis and pair of (TPR,FPR) are displayed on the graph :

![image](https://user-images.githubusercontent.com/38240162/72688396-b7eba780-3afe-11ea-9631-dcad32926a28.png)

**Hold Out:** Hold-out is when you split up your dataset into a ‘train’ and ‘test’ set. 
The training set is what the model is trained on, and the test set is used to see how well that model performs on unseen data. 
A common split when using the hold-out method is using 80% of data for training and the remaining 20% of the data for testing.

**Cross Validation Method:** Cross-validation or ‘k-fold cross-validation’ is when the dataset is randomly split up into ‘k’ groups. 
One of the groups is used as the test set and the rest are used as the training set. 
The model is trained on the training set and scored on the test set. Then the process is repeated until each unique group as been used as the test set.

**CONCLUSION:** Various technique to evaluate the performance of classifiers applied on various dataset are shown above with examples.
