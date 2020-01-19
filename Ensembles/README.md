# ENSEMBLES

**PROGRAMMING LANGUAGE USED:** Python 3.x

**IDE:** Jupyter

**TASKS:**
1. Bagging 
2. Random Subspace 
3. Boosting
4. Feature Importance from Random Forests

Dataset Used: Hotel Review Dataset

**Ensembles:**Ensemble methods is a machine learning technique that combines several base models in order to produce one optimal predictive model.

**Bagging** BAGGing, or Bootstrap AGGregating. BAGGing gets its name because it combines Bootstrapping and Aggregation to form one ensemble model. 

![image](https://user-images.githubusercontent.com/38240162/72690162-64368980-3b11-11ea-9113-d2e2373cbada.png)

**Boosting:**
Step 1: The base algorithm reads the data and assigns equal weight to each sample observation.
Step 2: False predictions made by the base learner are identified. In the next iteration, these false predictions are assigned to the next base learner with a higher weightage on these incorrect predictions.
Step 3: Repeat step 2 until the algorithm can correctly classify the output.
Therefore, the main aim of Boosting is to focus more on miss-classified predictions.

![image](https://user-images.githubusercontent.com/38240162/72690519-102da400-3b15-11ea-89cf-e64e6401ec9a.png)

**Feature Importance from Random Forests:**
Random Forest Models can be thought of as BAGGing, with a slight tweak. 
When deciding where to split and how to make decisions, BAGGed Decision Trees have the full disposal of features to choose from. Therefore, although the bootstrapped samples may be slightly different, the data is largely going to break off at the same features throughout each model. In contrary, Random Forest models decide where to split based on a random selection of features. Rather than splitting at similar features at each node throughout, Random Forest models implement a level of differentiation because each tree will split based on different features.

**CONCLUSION:** Ensembles through Bagging, bossting are executed and shown above.
