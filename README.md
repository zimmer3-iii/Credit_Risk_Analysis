# Credit_Risk_Analysis

## Overview
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Then I evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

### Oversampling
- `Accurarcy score:` 0.6620175698580149
- `Confusion Matrix:` 

|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 73              |               28 |
| `Actually False`  | 6820            |            10284 |

- `Classification Report:`

|                   | `pre`| `rec`| `spe`| `f1` | `geo`| `iba`| `sup` |
| ----------------- |:----:| ----:| ----:| ----:| ----:| ----:| -----:|
| `high_risk`       | 0.01 | 0.72 | 0.60 | 0.02 | 0.66 | 0.44 | 101   |
| `low_risk`        | 1.00 | 0.60 | 0.72 | 0.75 | 0.66 | 0.43 | 17104 |
| `avg / total`     | 0.99 | 0.60 | 0.72 | 0.75 | 0.66 | 0.43 | 17205 |

### SMOTE Oversampling
- `Accurarcy score:` 0.6568196079430206
- `Confusion Matrix:` 

|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 62              |               39 |
| `Actually False`  | 5135            |            11969 |

- `Classification Report:`

|                   | `pre`| `rec`| `spe`| `f1` | `geo`| `iba`| `sup` |
| ----------------- |:----:| ----:| ----:| ----:| ----:| ----:| -----:|
| `high_risk`       | 0.01 | 0.61 | 0.70 | 0.02 | 0.66 | 0.43 | 101   |
| `low_risk`        | 1.00 | 0.70 | 0.61 | 0.82 | 0.66 | 0.43 | 17104 |
| `avg / total`     | 0.99 | 0.70 | 0.61 | 0.82 | 0.66 | 0.43 | 17205 |

### Undersampling
- `Accurarcy score:` 0.5447339051023905
- `Confusion Matrix:` 

|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 70              |               31 |
| `Actually False`  | 10324           |            6780  |

- `Classification Report:`

|                   | `pre`| `rec`| `spe`| `f1` | `geo`| `iba`| `sup` |
| ----------------- |:----:| ----:| ----:| ----:| ----:| ----:| -----:|
| `high_risk`       | 0.01 | 0.69 | 0.40 | 0.01 | 0.52 | 0.28 | 101   |
| `low_risk`        | 1.00 | 0.40 | 0.69 | 0.57 | 0.52 | 0.27 | 17104 |
| `avg / total`     | 0.99 | 0.40 | 0.69 | 0.56 | 0.52 | 0.27 | 17205 |

### Combination (Over and Under) Sampling
- `Accurarcy score:` 0.6778933652252035
- `Confusion Matrix:` 

|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 79              |               22 |
| `Actually False`  | 7293            |            9811  |

- `Classification Report:`

|                   | `pre`| `rec`| `spe`| `f1` | `geo`| `iba`| `sup` |
| ----------------- |:----:| ----:| ----:| ----:| ----:| ----:| -----:|
| `high_risk`       | 0.01 | 0.78 | 0.57 | 0.02 | 0.67 | 0.46 | 101   |
| `low_risk`        | 1.00 | 0.57 | 0.78 | 0.73 | 0.67 | 0.44 | 17104 |
| `avg / total`     | 0.99 | 0.57 | 0.78 | 0.72 | 0.67 | 0.44 | 17205 |

### Balanced Random Forest Classifer
- `Accurarcy score:` 0.7885466545953005
- `Confusion Matrix:` 

|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 71              |               30 |
| `Actually False`  | 2153            |            14951 |

- `Classification Report:`

|                   | `pre`| `rec`| `spe`| `f1` | `geo`| `iba`| `sup` |
| ----------------- |:----:| ----:| ----:| ----:| ----:| ----:| -----:|
| `high_risk`       | 0.03 | 0.70 | 0.87 | 0.06 | 0.78 | 0.60 | 101   |
| `low_risk`        | 1.00 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17104 |
| `avg / total`     | 0.99 | 0.87 | 0.70 | 0.93 | 0.78 | 0.62 | 17205 |

### Easy Ensemble AdaBoost Classifer
- `Accurarcy score:` 0.9316600714093861
- `Confusion Matrix:` 

|                   | `Predicted True`| `Predicted False`|
| ----------------- |:---------------:| ----------------:|
| `Actually True`   | 93              |               8  |
| `Actually False`  | 983             |            16121 |

- `Classification Report:`

|                   | `pre`| `rec`| `spe`| `f1` | `geo`| `iba`| `sup` |
| ----------------- |:----:| ----:| ----:| ----:| ----:| ----:| -----:|
| `high_risk`       | 0.09 | 0.92 | 0.94 | 0.16 | 0.93 | 0.87 | 101   |
| `low_risk`        | 1.00 | 0.94 | 0.92 | 0.97 | 0.93 | 0.87 | 17104 |
| `avg / total`     | 0.99 | 0.94 | 0.92 | 0.97 | 0.93 | 0.87 | 17205 |