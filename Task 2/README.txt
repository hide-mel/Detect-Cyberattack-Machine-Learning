Read the following before looking into the files


Main program:

1132300_KatsuhideI_Task2.ipynb:
read the provided csv files
preprocess the data and encode the categorical values.
encode labels to -1 or 1, 1 is anomaly and -1 is normal
feature selection by kbest using chi2
prediction using logistic regression
produce the score of accuracy f1 precision recall
data insight: frequencies of items in predicted anomalies
pickup 1 IP address and make adversial samples
do prediction again to see if adversial samples could bypass the anomaly detection


Other Files (provided files):

training_data_with_label.csv, test_data_with_label.csv, validation_data_with_label.csv: provided datasets