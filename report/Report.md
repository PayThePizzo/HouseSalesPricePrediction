Report
Explorative Data Analysis
Problem definition
The target of this analysis is to assess the value of a house, basing on the data provided by the Zillow platform.
Since the database is not made for that, we can predict the log-error, which is a measure that allows the protection of the houses owners’ sensitive data.
The housing-market in the west coast of the U.S.A.
We need to consider some biases that could emerge from our predictions:
1. We are focusing on a particular geographical area, which we are not familiar with;
2. We are focusing on a market we have no prior domain-knowledge of;
3. There is no price sale in the dataset, for the reason mentioned before.
Dataset cleaning
We used a vast variety of cleaning and feature engineering strategies to converge to a usable training dataset. We can resume them in the following main steps:
1. Basic Exploration
2. Data Cleaning & Feature Engineering
3. Modeling
4. Export
Step 1: Basic Exploration
After importing our data and setting up our environment, we extracted the main basic information from the datasets (shape, dimension, number and types of the features…).
We then merged our tables using what substantially is a NATURAL JOIN operation between the properties datasets and the train datasets.
Step 2: Data Cleaning & Feature Engineering
At this point we identified the amount of missing data, and deleted the feature whose information could not be retrieved in any way. We established that a missing data rate above 89% is a good threshold to consider for dropping our columns.
After that, we analyzed the existing correlations between the remaining features. It was obvious that there was a good number of features with high correlation, and therefore a consistent redundancy between the data.
The following step was identifying the outliers in the logerror feature, which is the one that we want to predict.
Step 3: Modeling
We are going to manipulate the existing features to better direct our predictions.
Some of these columns are not useful for our purpose, this is why after an extensive research we understood the main driving factors for house prices:
1. Neighborhood comps
2. Location
3. Home size and usable space
4. Age and condition
5. Upgrades and updates
6. The local market and economic change
8. Mortgage interest rate
However, we do not have data for each one of those points and most of them are hard to represent in the way the datasets are given to us (even if we wanted to add some features of our own).
During this step, we had to face some difficult decisions:
Type Conversion: some values were adapted to better fit our models.
Rescaling: some features were using some scales that were difficult to use.
Additional features: we added some features that could lower the entropy of the existing data by resuming some redundant ones in a unique feature. Further details are contained in the notebook.
Dropping Values: it is critical to keep the dataset as light as possible, in order to reduce the computational time needed, so we deleted some data that may derail our predictions, in particular:
Outliers;
Empty Columns;
 Artificial Filling (if over 60%): in some cases, the missing data were just numerical 0 values that were not inserted correctly in the dataset, so we handled them by converting to the correct value.
At the end of this step, we used the XGBoost algorithm to assert which features resulted to be the most influential.
Step 4: Export
After the cleanup, we prepared the dataset for the prediction phase. Before exporting the dataset, we splitted it by using the k-fold method, in order to obtain a cross validation. This allowed us to prevent the overfitting and the low prediction power of our models. 
We also decided to train the models using the aforementioned dataset, and to conduct the test using the 2017 dataset, in order to increase the accuracy of our test and to lower the biases as much as possible.
Predictions
Gianmaria Pizzo
Random Forest

ANN


Marco Terrin
Niccolò Simonato
K-NN
Why?
I chose the k-NN algorithm because, usually, the house construction doesn't happen randomly. Usually the constructions are planned with great detail.
Therefore, the k-NN aims to catch the consequential correlations.
After an initial tuning of the features, the models were trained using different parameters in order to test as many configurations as possible.
The number of neighbors was considered to be between 4 and 8, because usually these are the values that yield the best results.
Considerations - Results
Linear Regression
Why?
The LinReg model was adopted due to the low integrity of the initial dataset. 
In contrast with the previously analyzed model, this is an attempt to see what would happen with an "assumption-free" model. It is expected that this type of analysis will underline some unseen and unexpected correlations, and also will produce some interesting predictions.
The evaluation tests were conducted by using the Mean Squared Error and the R-squared indexes.
Considerations - Results
Final Considerations
