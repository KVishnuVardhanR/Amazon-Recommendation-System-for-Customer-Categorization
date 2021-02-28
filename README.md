# Amazon-Recommendation-System-for-Customer-Categorization
Recommender systems are the systems that are designed to recommend things to the user based on many different factors. These systems predict the most likely product that the users are most likely to purchase and are of interest to. Companies like Netflix, Amazon, etc. use recommender systems to help their users to identify the correct product or movies for them. 

# Getting started
- The data is first subjected to data preparation techniques: Imputing missing values using **KNN Imputer** for numerical data, replace missing values with mode for categorical data. Checking whether any data is duplicated or not will help the model to get improved.
- Finding outliers is necessary, especially for categorizing, The outliers can be dealt by replacing them with **IQR[Inter Quartile Range]**.   
- As the given training data is Imbalanced, We have to avoid basic approaches like using train-test-split, normal cross validation techniques and accuracy metric for measuring, so that the model wouldn’t get biased towards a particular label.
- Instead we can use bagging and boosting techniques **[LightGBM,CatBoost]** for classification purposes, Usage of StratifiedKFold cross validation technique will make sure that train and validation sets have both the labels to avoid overfitting, metrics such as presicion, recall, ROC curve will help get us insights on how well the classifier is performing.
- After through validating and fine tuning, the model is then deployed in the E- commerce platform. As the new data comes in, we train the model and find the sweet spot of our model and then deploy it again, and this process continues.

