**<h2>MACHINE LEARNING INTERVIEW QUESTIONS</h2>**

<h3>1. What do you understand by Machine Learning ?</h3>

Potential Answer: Machine learning is a tool for turning information into knowledge. 
  
   We are drowning in information and starving for knowledge. Enormous amount of data is being generated on a daily basis. There's no use of this data unless we analyse for the under lying patterns within the data.
  
   Traditionally, software engineering combined human created rules with data to create answers to a problem. Instead, machine learning uses data and answers to discover the rules behind a problem.
  
   To learn the rules governing a phenomenon, machines have to go through a learning process, trying different rules and learning from how well they perform. Hence, why it’s known as Machine Learning.
  
   Machine learns through experiences using statistical methods without being explicitly programmed.
  
  ![image](https://user-images.githubusercontent.com/38240162/90568575-13b90480-e1a4-11ea-931b-135ab5be3322.png)
 
  
  
<h3>2. What is Supervised and Unsupervised Learning ?</h3>

Potential Answer:  

Supervised Learning: Labelled Data, Regression & classification, Map labelled input to output.

The algorithm learns on a labeled dataset, providing an answer key that the algorithm can use to evaluate its accuracy on training data. 

It develops a predictive model based on both input and output.

![image](https://user-images.githubusercontent.com/38240162/90569357-a8703200-e1a5-11ea-92ec-4f5c71c255cb.png)

Unsupervised Learning: Unlabeled Data, Association & Clustering, understand pattern and discover output.

It provides unlabeled data that the algorithm tries to make sense of by extracting features and patterns on its own.

It groups and interpret the data based on the input data only.

![image](https://user-images.githubusercontent.com/38240162/90569316-955d6200-e1a5-11ea-9a57-c6e2f8ed8fed.png)



<h3>3. What do you understand by Precision and Recall?</h3>
Potential Answer:  Let me explain you this with an analogy:

Imagine that, your girlfriend gave you a birthday surprise every year for the last 10 years. One day, your girlfriend asks you: ‘Sweetie, do you remember all the birthday surprises from me?’
To stay on good terms with your girlfriend, you need to recall all the 10 events from your memory. Therefore, recall is the ratio of the number of events you can correctly recall, to the total number of events.
If you can recall all 10 events correctly, then, your recall ratio is 1.0 (100%) and if you can recall 7 events correctly, your recall ratio is 0.7 (70%)
However, you might be wrong in some answers.
Recall/Sensitivity/True Positive Rate(TPR): (TP/TP+FN)

For example, let’s assume that you took 15 guesses out of which 10 were correct and 5 were wrong. This means that you can recall all events but not so precisely
Therefore, precision is the ratio of a number of events you can correctly recall, to the total number of events you can recall (mix of correct and wrong recalls).
From the above example (10 real events, 15 answers: 10 correct, 5 wrong), you get 100% recall but your precision is only 66.67% (10 / 15)
Precision: (TP/TP+FP)
  
  
<h3>4. Explain the concept of Decision Tree.</h3>

Pointers to remember:
  1. Supervised ML technique
  2. Used for both Classification and Regression technique, aka "CART".
  3. Whatever knowledge Dec Tree learns through training phase, it formulates that to a hierarchical structure.
  4. It consists of 2 steps:
    
    a. Induction (Process of building of decision tree)
    
    b. Pruning (Removal of unnecessary branches from the tree which do not contribute to the predictive power of classifier.)
    
Links to refer:

1. https://towardsdatascience.com/decision-trees-in-machine-learning-641b9c4e8052
  
2. https://www.displayr.com/machine-learning-pruning-decision-trees/#:~:text=Pruning%20reduces%20the%20size%20of,pruning%20can%20reduce%20this%20likelihood.
  
3. https://saedsayad.com/decision_tree_reg.htm#:~:text=The%20ID3%20algorithm%20can%20be,Gain%20with%20Standard%20Deviation%20Reduction.&text=A%20decision%20tree%20is%20built,with%20similar%20values%20(homogenous).
  
4. https://towardsdatascience.com/a-guide-to-decision-trees-for-machine-learning-and-data-science-fe2607241956

<h3>5. Ways to handle imbalanced data </h3>

Potential Answer:

Imbalanced Dataset: Classification task where the classes are not equally distributed.

Ways to handle them:

1. Use appropriate evaluation metric.
2. Resampling:
  2a. Undersampling
  2b. Oversampling
3. Cross-Validation
4. Ensemble of resampled dataset.
5. Resample of different ratio.


Links to refer:
1. https://www.kdnuggets.com/2017/06/7-techniques-handle-imbalanced-data.html
2. https://www.researchgate.net/post/How_10-fold_cross_validation_helps_to_handle_the_imbalance_data_set
  

<h3>6. Bias- Variance Trade Off </h3>

Links to refer:

1. https://towardsdatascience.com/top-30-data-science-interview-questions-7dd9a96d3f5c
2. https://towardsdatascience.com/understanding-the-bias-variance-tradeoff-165e6942b229

![image](https://user-images.githubusercontent.com/38240162/91093394-473ad980-e651-11ea-90ff-ed392e9de4f8.png)

![image](https://user-images.githubusercontent.com/38240162/91093492-6c2f4c80-e651-11ea-9560-0aea750c3bdd.png)

![image](https://user-images.githubusercontent.com/38240162/91093530-7c472c00-e651-11ea-8c70-98d2ebd3bb85.png)


<h3>7. Explain the concept of Cross Validation: </h3>
Potential Answer:

Cross-validation is a statistical method used to estimate the skill of machine learning models. It is a resampling procedure to evaluate ML models on a limited dataset.

**k in K-fold Cross Validation is the number of groups that a given data sample is to be split into.**

Procedure:
  1. Shuffle the dataset randomly.
  2. Split the dataset into k groups
  3. For each unique group:
      3.1 Take the group as a hold out or test data set.
      
      3.2 Take the remaining groups as a training data set.
      
      3.3 Fit a model on the training set and evaluate it on the test set.
      
      3.4 Retain the evaluation score and discard the model.
  4. Summarize the skill of the model using the sample of model evaluation scores

Links to refer:
1. https://towardsdatascience.com/why-and-how-to-cross-validate-a-model-d6424b45261f
2. https://machinelearningmastery.com/k-fold-cross-validation/
3. https://stats.stackexchange.com/questions/416553/can-k-fold-cross-validation-cause-overfitting


<h3>8. Explain the concept of Logistic Regression.

Links to refer:
1. https://towardsdatascience.com/introduction-to-logistic-regression-66248243c148

2. https://towardsdatascience.com/understanding-logistic-regression-9b02c2aec102
  
![image](https://user-images.githubusercontent.com/26432753/90569620-1b79a880-e1a6-11ea-8030-879e3fd2891d.png)


<h3>9. Explain the concept of Random Forest.</h3>

Points to remember:
  
  1. Supervised ML technique
  
  2. Used for both Classification and Regression tasks.
  
  3. It uses a group of uncorelated decision trees which acts as a group, ense,ble outperforms any individual decision tree.
  
  4. Two things it considers:
      
      a. Random sampling of the training data when building the random forest.
      
      b. Random subset of features when splitting the node.
  
  5. The random forest combines hundreds or thousands of decision trees, trains each one on a slightly different set of the observations, splitting nodes in each tree considering a limited number of the features. The final predictions of the random forest are made by averaging the predictions of each individual tree.
  
  
Links to refer:

1. https://towardsdatascience.com/an-implementation-and-explanation-of-the-random-forest-in-python-77bf308a9b76

2. https://towardsdatascience.com/understanding-random-forest-58381e0602d2


<h3>10. Naive Bayes Concept: </h3>
 
Potential Answer: 
Naive Bayes is a probabilisitic ML model based on Bayes algorithm. It is majorly used for Classification tasks.

![image](https://user-images.githubusercontent.com/38240162/91096728-69832600-e656-11ea-9f6a-9323b7b9bed8.png)

Advantages:
  1. Easy to implement.
  2. Fast execution.
  3. Used for Sentiment Analysis, Recommender System.
  4. Performs better than more complicated models when the data set is small.
  
Disadvantages:
  1. The requirement of predictors to be independent.
  
Link to refer:
 
1. https://towardsdatascience.com/naive-bayes-classifier-81d512f50a7c


**<h2>DEEP LEARNING INTERVIEW QUESTIONS</h2>**

<h3>1. What is the need of deep learning if Machine Learning can solve?</h3>

Links to refer: 

https://quantdare.com/what-is-the-difference-between-deep-learning-and-machine-learning/

**REFERENCES:**

Medium. 2020. Machine Learning | An Introduction. [online] Available at: <https://towardsdatascience.com/machine-learning-an-introduction-23b84d51e6d0> [Accessed 28 July 2020].

