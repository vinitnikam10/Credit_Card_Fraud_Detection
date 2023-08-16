# Credit_Card_Fraud_Detection
## Credit card fraud detection project

Credit Card Fraud Detection with Machine Learning is a process of data investigation and the development of a model that will provide the best results in
revealing and preventing fraudulent transactions. This is achieved through bringing together all meaningful features of card users’ transactions, such as Date, User Zone, Product Category, Amount, Provider, Client’s Behavioral Patterns, etc. The information is then run through a subtly trained model that finds patterns and rules so that it can classify whether a transaction is fraudulent or legitimate.

### About Dataset :
The dataset contains transactions made by credit cards in September 2013 by European cardholders.

### Evaluation Metrics:
Given the class imbalance ratio, we recommend measuring the accuracy using the Area Under the Precision-Recall Curve (AUPRC). Confusion matrix accuracy is not meaningful for unbalanced classification.

### EDA and Data Pre-processing:
After using .skew() function came to know that some column values have skewed data. So we used the cube root function to remove the skewness of the data. The Amount column is not standardized so we use the StandardScaler() from sklearn to standardize the data.

### Building the model:
So first create a function in which we had defined our model. First, we split the dataset as train and test with the split percentage of 0.3. then we called the LogisticRegression(), GaussianNB(), SVC(), XGBClassifier(), DecisionTreeClassifier() Classifiers from the sklearn library, an then fitted, predicted the data, and print the confusion matrics, classification report, and the precision, recall, F1 score and the accuracy of the model.

### Using SMOTE :
As our dataset is imbalanced the models are not able to predict well. So we need to balance out our data set. For this, we will be using the SMOTE: Synthetic Minority Oversampling Technique. SMOTE is an oversampling technique where the synthetic samples are generated for the minority class. This algorithm helps to overcome the overfitting problem posed by random oversampling. It focuses on the feature space to generate new instances with the help of interpolation between the positive instances that lie together.

### Using Deep Learning:
Using the Deep neural network our score improved even more Accuracy: 0.999695, Precision: 0.999392, Recall: 1.000000, F1_score: 0.999696. We achieved Recall = 1 i.e we had not predicted any fraud as the nonfraud transaction.
