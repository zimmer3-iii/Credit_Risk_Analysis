# Credit_Risk_Analysis

## Overview
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Then I evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

#### Oversampling
- Accurarcy score: 0.6620175698580149
- Confusion Matrix: 
|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 73              |               28 |
| `Actually False`  | 6820            |            10284 |
