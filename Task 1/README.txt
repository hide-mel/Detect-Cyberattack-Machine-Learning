Please read the following before looking into the files.

I have included CSV files: splunk_training_data, splunk_test_data, and splunk_validation_data_with_label.
because they are generated from my splunk setting and necessary for the program. 


Main program:
1132300_KatsuhideI_Task1_Data_Encoder.ipynb: 
preprocessing the data and export encoded-train.csv, encoded-test.csv, encoded-valid.csv.
encode validation label to 1 or -1; 1 is anomaly-1 is normal.
encode categorical values to numerical.
run this first

1132300_KatsuhideI_Task1_Prediction.ipynb:
feature selection using variance threshold and correlation base
prediction using isolation forest and local outlier factor
gridsearchcv for parameter turning
data insight: check the frequencies of items in predicted label
output TXT file (1132300_task1.txt) that contains only steam ID of predicted anomalies 
run this second


Other Files (provided and producded from the programs/splunk):
1132300_task1.txt: contains only steam ID of predicted anomalies
encoded-train.csv, encoded-test.csv, encoded-valid.csv: encoded csv files made by 1132300_KatsuhideI_Task1_Data_Encoder.ipynb
splunk_test_data.csv, splunk_training_data.csv, splunk_valid_data.csv: splunk processed/generated data that was transformed from the provided csv files
training_data.csv, test_data.csv, validation_data_with_label.csv: provided datasets