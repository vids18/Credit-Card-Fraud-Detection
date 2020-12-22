# Credit Card Fraud Detection
This repository is made for the display of my final semester graduate Capstone project.

1. Inspiration

With the growth of the e-commerce industry and community and the dire to make the global economy cashless, there have been people choosing digital payments over cash. Fraud is a huge national and worldwide problem; we will see credit card fraud rise at rates faster than ever. Credit card fraud is a form of identity theft involving criminal deception for personal financial gain. Here are some quick stats about credit card frauds:

*	There were 650,572 cases of identity theft in the U.S. in 2019. Of those, 41 percent, or just over 270,000, were credit card fraud
* In 2018, $24.26 Billion was lost due to payment card fraud worldwide
* Credit card fraud was ranked #1 type of Identity theft fraud
* The United States leads as the most credit fraud-prone country with 38.6% of reported card fraud losses in 2018

To identify the factors leading to scams and minimize their extent, I decided to build a project that recognizes whether the transaction is a fraud or genuine.

2. Datasets

To perform analysis and build a model that correctly identifies the transaction, I have used two datasets: German Credit data by UCI Machine Learning and Credit Card Fraud Detection by Machine Learning Group-ULB from Kaggle. 

* The German credit data is a fantastic dataset with variables that help decide whether a person is a good credit risk or a bad credit risk. There are originally 1000 entries and nine attributes in the dataset. 
* The second dataset contains transactions made by credit cards in September 2013 in a span of two days. Therefore, I have about 284807 transactions and 31 columns containing only numerical input values resulting from PCA transformation. 

3. Data Dictionary

German credit dataset has nine selected attributes that are important for analysis.

*	Age (numeric)
* Sex (text: male, female)
* Job (numeric: 0- unskilled and non-resident, 1- unskilled and resident, 2- skilled, 3- highly skilled)
* Housing (text: own, rent, free)
* Savings account (text: little, moderate, quite rich, rich)
* Checking's account (numeric)
* Credit amount (numeric)
* Duration (numeric in months)
* Purpose (text: car, furniture/equipment, radio/TV, domestic appliances, repairs, education, business, vacation/others)

Unfortunately, due to confidentiality issues, credit card fraud detection by ULB cannot provide the original features and more background information of the data. Features V1, V2, … V28 is the principal components obtained with PCA; the only non-transformed parts with PCA are 'Time' and 'Amount.'

* Time (numeric: seconds elapsed between each transaction and the first transaction in the dataset)
* Amount (numeric: transaction amount)
* Class (Target variable, numeric values: 1- fraud, 0- non-fraud)

4. Conclusion

There are many criteria's like F1_score, precision, recall, accuracy score, ROC-AUC values for choosing and evaluating the best model. I have compared the confusion matrix, F1_score, precision, recall, accuracy score, and AUC values. My problem is to detect whether a transaction is a scam or a genuine one; I cannot afford a fraud classified as a non-fraud.  Choosing a model with the highest recall (specificity) is of utmost importance. The values calculated in the above table show Decision Tree and Random Forest models, giving a recall score of 0.99. 

Since there is a tradeoff between the two models, the next metric to consider is the ROC-AUC curve and the accuracy. The difference between the Accuracy and ROC-AUC curve values is that the former is calculated based on predicted classes while the latter on predicted scores. The ROC-AUC value for Random Forest is the maximum (0.99), i.e., most of my fraud transactions classify frauds and vice versa. Thus, in conclusion, Random Forest Classification serves as the best model for my implementation.



