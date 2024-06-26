# credit-risk-classification

In this project, various techniques were employed to train and evaluate a model for assessing loan risk. Leveraging a dataset of historical lending activity from a peer-to-peer lending services company, a model was developed to discern the creditworthiness of borrowers.


## Split the Data into Training and Testing Sets
The initial step involved importing the lending_data.csv dataset from the resources folder into a Pandas DataFrame. Subsequently, a labels set (y) was created from the “loan_status” column, while the features (X) DataFrame was extracted from the remaining columns. Upon examining the value counts of the label set, it became evident that there was a significant imbalance between class labels (class 0 = 75036; class 1 = 2500). To mitigate the bias towards the majority class in logistic regression, which may lead to poor detection of the minority class and misleading metrics, resampling techniques were employed to balance the dataset. The data were then split into training and testing sets using train_test_split.


![Balance data set](https://github.com/MarcoN16/credit-risk-classification/assets/150491559/3e1c8006-d92d-411b-82bf-682d72195ea9)


## Create a Logistic Regression Model
A logistic regression model was created using sklearn library. The model was trained using the training dataset (X_train and y_train). Subsequently, model has been tested on the testing dataset. Lastly, model performance was evaluated by generating a confusion matrix and a classification report.

## Performance Analysis Report
The analysis aimed to develop a robust model for assessing loan risk, leveraging a comprehensive dataset of historical lending activities. Within the dataset, a value of 0 in the "loan_status" column signifies a healthy loan, while a value of 1 indicates a high risk of default. Key functions imported from the sklearn library included confusion_matrix and classification_report were used to analyze the results. The resulting classification report showcased remarkable accuracy on the test data, as evidenced by the following metrics:

-	True Positive: 625
-	False Positive: 4
-	False Negative: 0
-	True Negative: 621

Further calculations of precision, recall, and accuracy underscored the model's exceptional performance:

- Precision for identifying status = 0: 99% and status = 1: 100%, indicating minimal misclassification of false positives for loans classified as bad.
-	Recall for identifying status = 0: 100% and status = 1: 99%, indicating minimal misclassification of false negatives.

<img width="432" alt="Classification_report" src="https://github.com/MarcoN16/credit-risk-classification/assets/150491559/5c84fb25-db84-4bb3-bd22-a2db82a3f306">


## Conclusion

The model demonstrated robust performance in discriminating the creditworthiness of borrowers. Similar results have been observed when employing the AdaBoostClassifier. Notably, the accuracy across testing and training data remained consistent, mitigating concerns regarding overfitting. This model holds significant utility within a company's loan classification process, offering high accuracy in discerning loan statuses and minimizing errors. This model can be utilized by the company for future loan classifications. Nevertheless, continuous testing of new data and a focus on mitigating misclassifications, particularly regarding loans at high risk of default, are essential precautionary measures to minimize potential adverse impacts resulting from incorrect classifications.


# References
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.

