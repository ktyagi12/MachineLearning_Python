# DIMENSIONALITY REDUCTION TECHNIQUES

**PROGRAMMING LANGUAGE USED:** Python 3.x

**IDE:** Jupyter

**AIM:**  Identify good feature subsets using the training dataset and test these subsets on the test data.

**Case I: NONE Feature Selection**
Here,there's no feature selection strategy is incorporated.
All the features are considered while calculating the accuracy on test data as well on train data using hold out and cross validation respectively.

Gradient boosting is a machine learning technique for regression and classification issues that produces a predictive model in the form of a collection of weak predictive models. It builds the model in a stage-wise fashion and generalizes it by allowing optimization of an arbitrary differentiable loss function.
The ensemble problem is simplified greedily as a forward stage-wise additive model. We don’t optimize the ensemble in a global manner, but instead seek to improve the result based on the current estimate.

**Case II: Feature Selection using INFORMATION GAIN**
Information gain (IG) measures how much “information” a feature gives us about the target class.
Features out of total number of features which are having high mutual dependency with the target variable are extracted first.
Then instead of training the model on whole dataset, model is build using only the extracted features.
Then classification of unknown values with only extracted features is done.
Thus computation complexity reduces as compared to training the model with all the features.
In case of a classification task, we measure the dependence between each feature and the target variable. If there exists a dependence, then we extract that feature for our classification tasks.

**Select k best features**
We rank the features using information gain (well mutual information) and select the k best to build a classifier.
We iterate through increasing values of k.
SelectKBest is a transform that transforms the training data.
The k best features out of 44 which are having high accuracy from the classifier passed(mutual_info_classif) are extracted.
Training and test data is transformed according to the number of features extracted.
Then it learns the model parameters.
(Hold out Method): Prediction for the class of test data is done using the trained classifier.
(Cross Val Method): Cross validation is performed on the training data to calculate its accuracy

**Case III: Feature Selection using Wrapper-based forward sequential search**
scikit learn does not support Wrapper feature selection so we use MLxtend.
Wrapper methods are based on greedy search algorithms as they evaluate all possible combinations of the features and select the combination that produces the best result for a specific machine learning algorithm.
Step Forward Feature Selection: In the first phase,the performance of the classifier is evaluated corressponding to each feature. The feature that performs the best is selected out of all the features.
Next step, the first feature is tried in combination with all the other features. The combination of two features that yield the best algorithm performance is selected.
Similarly, the process continues until the specified number of features are selected.
k_features specifies the number of features to select. The forward parameter, if set to True, performs step forward feature selection. The verbose parameter is used for logging the progress of the feature selector. The scoring parameter defines the performance evaluation criteria. Finally, cv refers to cross-validation folds.
Thus a feature selector is created using the SFS(). Now the fit method is invoked on the feature selector and pass it the training and test sets.

**Case IV: Feature Selection using Wrapper-based backward elimination.**
scikit learn does not support Wrapper feature selection so we use MLxtend.

Wrapper based backward elimination is a step backwards feature selection. It is the exact opposite of step forward feature selection. In the first phase, one feature is removed in round-robin fashion from the feature set and the performance of the classifier is evaluated.
The feature set that yields the best performance is retained.
In the second step, again one feature is removed in a round-robin fashion and the performance of all the combination of features except the 2 features is evaluated.
This process continues until the specified number of features remain in the dataset.
k_features specifies the number of features to select. The forward parameter, if set to False, performs step backward feature selection. The verbose parameter is used for logging the progress of the feature selector. The scoring parameter defines the performance evaluation criteria. Finally, cv refers to cross-validation folds.
Thus a feature selector is created using the SFS(forward = False). Now the fit method is invoked on the feature selector and pass it the training and test sets.

**CONCLUSION:**

FILTER METHOD: The Information Gain filter is classifier agnostic pre-selection method which are independent of the machine learning method. This is computationally more efficient but selection of features may depend on the learning algorithm which it ignores.

WRAPPER METHOD: Wrappers are feedback methods which incorporate the Machine Learning algorithm in the Feature Selection process,i.e they rely on the performance of a specific classifier to evaluate the quality of a set of features. Wrapper methods search through the space of feature subsets and calculate the estimated accuracy of a single learning algorithm for each feature that can be added to or removed from the feature subset.

The accuracy on the test data calculated using all 3 feature selection strategies (Information Gain Filter, Wrapper Sequential Forward Selection, Wrapper based Backward elimination) comes to be consistent whereas accuracy on the training dataset is eventually increasing in case of Wrapper methods.
The filter method is unstable as compared to the Wrapper based methods because:

No Model Bias: Different features may suit different learning algorithms but filters do not take this into account.

1. No Feature Dependencies: • The features are considered in isolation from one another, and are not considered in context. • In some cases, a filter might select two predictive but correlated features, where one would be sufficient. • In other cases, one feature needs another feature to boost accuracy, but a filter cannot discover this.
   whereas the Wrapper based methods considers bias into account and considers the features in context. The wrapper method is computationally more demanding, but takes dependencies of the feature subset on the learning algorithm into account.
2. Wrapper based Sequential Forward Selection method is faster than backward elimination technique as it starts with small subsets, so requires less running time if stopped early.
   It starts from 1 feature and goes upto the maximum accuracy bearing features but it's accuracy is less than that of the backward elimination strategy as once it gets the maximum accuracy in between, it will stop considering the next features 

The Wrapper based Backward Elimination strategy is slow but accuracy is high as it starts from combination of all the features calculating the accuracy and removing the feature one by one till no feature left.
The discrepancy between the training and test data can be accompanied by two facts:
  The training data set size is not even the half of the test dataset which may lead to overfitting.
  Using features extracted from wrapper methods can lead to overfitting as wrapper methods already train machine learning models with the features and it affects the true power of learning. But the features from filter methods will not lead to overfitting in most of the cases.

From the result graph, the accuracy on the test dataset is similar throughout the feature selection strategy but the accuracy on the training dataset in eventually increasing in the case of Wrapper based methods.
The insights on data that can be derived from the overall analysis of the data:
  1. Overfitting may happen due to the insufficient training data set.
  2. Filter methods may fail to find the best subset of features in situations when there is not enough data to model the statistical correlation of the features, but wrapper methods can always provide the best subset of features because of their exhaustive nature.
