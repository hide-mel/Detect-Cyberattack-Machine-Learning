# Detect-Cyberattack-Machine-Learning
 
# Project: Machine learning based cyberattack detection

# Overview: 
There are 2 tasks in this project: Task I aims to develop skills in applying unsupervised machine learning techniques for anomaly detection. Task II helps me better understand how to use gradient descent-based methods to generate adversarial samples against supervised learning models beyond the computer vision domain. 
(1) for Tasks I and II, two network traffic (NetFlow) datasets are provided, one for each task. Both datasets contain botnet traffic and normal traffic. I identify botnet IP addresses from both two datasets. (2) For Task II I also need to choose a botnet IP address, and explain how to manipulate the corresponding raw network traffic records in order to bypass detection. 

# Deliverables
1. Task I – Source code (Python) and SPL queries used to do the following:
a. Generate/Select features from the packet capture files (training and test datasets) using Splunk. 
b. Use two alternative feature generation/selection methods (filter-based, wrapper- based, etc.) to select features from packet capture files (training and test datasets). 
c. Use Python/Splunk to build six models: apply two different anomaly detection techniques on each of the three set of features generated/extracted from 1.a. and 1.b. 
d. Score the test data such that cyberattacks are assigned the highest (or lowest)1 scores. 
e. Return the IP addresses of attackers and the timestamps of their first and last attempt for attacking the network service (per attack scenario). 
f. Compare and discuss the results from different feature extraction and different anomaly detection techniques.
g. Prepare a TXT file including all stream ID which the program classifies as attack traffic, separated by newlines (i.e., one stream ID in each line). 
2. Task II
a.Source code in Python, including:
i. Building,trainingandtestingthesupervisedlearningmodel.
ii. Generating adversarial samples for a chosen botnet IP address, i.e., how to
modify its feature values. 
b. Explain how to change the raw traffic sent from/to the chosen botnet IP address, in order to reflect the modified feature values. For example, the following six features are extracted for each IP address: (1) mean outbound packet size, (2) variance of outbound packet size, (3) mean packet count per second, (4) max packet count per second, (5) mean of packet jitter, (6) variance of packet jitter. A supervised model is trained on these features to decide whether the corresponding IP address is malicious. You find that by manipulating the values of the third and fourth features, a botnet IP address is labelled as “normal” by the model. Then how do you change the raw traffic records so that they are consistent with the modified feature values? For instance, if 1000 raw traffic records were related to the bot, do you change all 1000 records, or only a subset, e.g., 100/200 of them? How do you change each of the selected traffic records? 

# Technical Report
Task I:
1. An overview of the test dataset using Splunk and explaining feature
generation/selection using SPL queries and Splunk native functionalities.
2. Description of my methodology for generating features. Briefly explain my method
for the first project, and discuss my modifications and new findings in this project.
3. Review of at least two anomaly detection methods that I have used.
4. Description of the experimental setup and evaluation of the (two) methods in
detecting anomalies on the test datasets using features generated in Splunk and also features generated using alternative methods. Description should also comprise IP addresses of attacker(s) and victim(s), the attacked service(s), the timestamp, and the type of the attack per attack scenario identified.
5. Description of my final CSV file, the scoring and thresholding technique I used for detecting the reported anomalies2.
6. Conclusion and discussion: describe anomaly detection method worked best given the attack scenario.
Task II:
7. Explanation of the generated features and my choice of supervised learning
model. Note that supervised learning is used here, and the mode is the target against which adversarial samples will be generated.
8. Choosing one IP address classified as botnet by my model, and explaining:
a. How to perturb its features via gradient descent-based method to bypass the
detection of my model;
b. How to change the raw network traffic sent from/to it, in order to be consistent
with the modified feature values and without affecting the botnet functionality.