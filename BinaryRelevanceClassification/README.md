## MULTI-LABEL CLASSIFICATION

**AIM:** Detect the multi labels a yeast gene is associated to.

**PROGRAMMING LANGUAGE:** Python

**IDE:** Jupyter Notebook

**ALGORITHM:** Decision Tree, Logistic Regression, RandomForest Classifier, Gaussian Naive Bayes

**INPUT:** Yeast Dataset

The Yeast dataset is formed by micro-array expression data and phylogenetic pro-files with 2,417 included. There are 103 descriptive features per gene. Each gene is associated with a set of functional classes. In this version of the dataset there are 14 functional classes and a gene can be associated with any number of these.

**TASKS:**

1. Implement the binary relevance algorithm, the simplest approach to multi-label classification is the binary relevance algorithm in which individual binary base classifiers are implemented for each label.

![image](https://user-images.githubusercontent.com/38240162/79005442-c4582d00-7b4e-11ea-8acf-837c510ad04c.png)

2. Using a grid -search, find out the best classifier in terms of performance.
3. In order to improve the performance and to create a balanced training dataset, undersample the data.
4. Compare the performance of the two different versions of the binary relevance classifier (with or without under-sampling).

![image](https://user-images.githubusercontent.com/38240162/79005765-860f3d80-7b4f-11ea-84fd-a1869b78c9bb.png)

5. The binary relevance classifier approach does not consider the associations between labels in a multilabel classification scenario. So as to compensate for this disadvantage, Implement the classifier chains algorithm, an effective multi-label classification algorithm that takes advantage of label associations.

![image](https://user-images.githubusercontent.com/38240162/79005497-e2259200-7b4e-11ea-8bbe-3e970662d9d5.png)

6. Compare the performance of the classifier chains algorithm to the versions of the binary relevance algorithm.

![image](https://user-images.githubusercontent.com/38240162/79005736-6f68e680-7b4f-11ea-92cf-115a62e155f2.png)

7. Reflect on the performance of the different models evaluated here. Consider model performance as well as computational requirements, and model complexity.


**CONCLUSION:**

Taking both the multi-label classification techniques into consideration following conclusions can be made:

1. Binary Relevance

__Accuracy Score__
* Binary Relevance classifier without undersampling produces the best 80% accuracy (Using Logistic Regression)  which is greater than any other undersampling model.
* We just under-sample a majority class if the gap between majority and minority is too big. This result in loss of accuracy due reduction in training samples and hence the overall accuracy.

__F1 Score__
* Without undersampling, the binary relevance classifier has lower F1 scores resulting in high bias that leads to high accuracy and poor recall values. 
* But after undersampling the gap between majority and minority class gets reduced which results in better F1 score.


|  | Logistic Regression | Decision Tree | Random Forest |
| -------|---------------------|---------------|---------------|
| __Accuracy Score__ | 0.80 | 0.65 | 0.77 |
| __F1 Score(macro avg)__ | 0.34 | 0.39 | 0.33 |


2. Classifier Chain

* Classifier chain works better than Binary Relevance because it takes label dependency into consideration. But if the output of the very first model comes wrong then the subsequent model output will be impacted badly.

* This approach has more complexity than binary relevance because it requires the previous target labels as input for the next predictions.

* However it can be seen that there is no substantial difference between the model accuracy which is quite unexpected.

|  | Logistic Regression |
| -------|---------------|
| __Accuracy Score__ | 0.8044 |
| __F1 Score(macro avg)__ | 0.3468 |


[Click here for the code](https://github.com/ktyagi12/MachineLearning_Python/tree/master/BinaryRelevanceClassification/code)

[Click here for the input](https://github.com/ktyagi12/MachineLearning_Python/tree/master/BinaryRelevanceClassification/input)


**REFERENCES:**

[1] Medium. (2018). Deep dive into multi-label classification..! (With detailed Case Study). [online] Available at: https://towardsdatascience.com/journey-to-the-center-of-multi-label-classification-384c40229bff [Accessed 8 Mar. 2020]. 

[2] Brownlee, J. (2020). Undersampling Algorithms for Imbalanced Classification. [online] Machine Learning Mastery. Available at: https://machinelearningmastery.com/undersampling-algorithms-for-imbalanced-classification/ [Accessed 8 Mar. 2020].

[3] S. (2020). Solving Multi-Label Classification problems (Case studies included). [online] Analytics Vidhya. Available at: https://www.analyticsvidhya.com/blog/2017/08/introduction-to-multi-label-classification/ [Accessed 8 Mar. 2020]. 
