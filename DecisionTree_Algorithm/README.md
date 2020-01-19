# SUPERVISED MACHINE LEARNING TECHNIQUE: Decision Tree

**PROGRAMMING LANGUAGE USED:** Python 3.x

**IDE:** Jupyter

**AIM:**  Use Decision Tree to identify the class of an unknown query using the concept of Entropy.

**TASKS:**
Dataset Used: ApplesPears, Iris, Athlete Selection 

1. Load the dataset
2. Normalise the data
3. Divide the input data into training data and test data
4. Predict the class for an test data.
5. Evaluate the performance of the classifier.

**Decision Tree:** A decision tree is a tree-like graph with nodes representing the place where we pick an attribute and ask a question; edges represent the answers the to the question; and the leaves represent the actual output or class label. They are used in non-linear decision making with simple linear decision surface.
Decision trees classify the examples by sorting them down the tree from the root to some leaf node, with the leaf node providing the classification to the example. 
Each node in the tree acts as a test case for some attribute, and each edge descending from that node corresponds to one of the possible answers to the test case. This process is recursive in nature and is repeated for every subtree rooted at the new nodes.

![image](https://user-images.githubusercontent.com/38240162/72687803-858b7b80-3af9-11ea-90b1-81fd7867ebd2.png)

**Entropy:** Entropy is a measure of randomness.

![image](https://user-images.githubusercontent.com/38240162/72687835-c2f00900-3af9-11ea-8111-8941a29c7649.png)

**Dealing with category data:** Convert the categorical data into numeric data - two options: 
1. get_dummies method for pandas.
2. OneHotEncoding for sklearn. 

**Pandas get_dummies**
The Pandas get_dummies method is the easiest way to do One-Hot encoding.
But if you want to apply the encoding to a test file later, this gets awkward. 

![image](https://user-images.githubusercontent.com/38240162/72687810-989e4b80-3af9-11ea-969c-0c1e514cf9fb.png)

**LabelEncoder** also converts category features to numbers
This is more compact. But it is not exactly what we want as the numbers are misleading.

![image](https://user-images.githubusercontent.com/38240162/72687818-a9e75800-3af9-11ea-9d25-8b46d323fba9.png)

**Using OneHotEncoding:**
OneHotEncoder class has two key methods: 
  1. fit to 'learn' the transform from the data,
  2. transform to apply the OneHot transform to the data, the transform can be applied to other (e.g. test) datasets.

**CONCLUSION:**
