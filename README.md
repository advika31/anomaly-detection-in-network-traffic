# Anomaly detection in Network traffic using Machine Learning

This document provides an overview of the steps involved in evaluating machine learning models for anomaly detection in network traffic. The following sections detail each phase of the model evaluation process.

## 01_PREPROCESSING

### Description
The dataset is loaded, and a subset (10%) of the data is sampled to expedite testing. Features and labels are identified, with labels combined into a single column for classification. Classes with insufficient samples are removed to ensure adequate data for model training and evaluation.

### Execution Time
The most recent runtime of this code was recorded as 43 seconds.

## 02_STATISTICS

### Description
This step analyzes the distribution of labels in the dataset. It categorizes labels into small, medium, and large groups based on their frequency and visualizes this distribution with horizontal bar charts. Additionally, it compares the percentage of benign versus attack instances.

Output: Bar charts showing label distribution and the percentage of benign vs. attack instances.

### Execution Time
The most recent runtime of this code was recorded as 4 seconds.

## 03_ATTACK FILTERING

### Description
This step filters attack samples from the dataset and creates separate files for each attack type. It ensures each attack file contains a balanced mix of attack and benign samples, with 30% of the samples being attacks and 70% being benign. The benign samples are randomly selected to match the required ratio.

Output: Separate CSV files for each attack type, saved in the ./attacks/ directory.

### Execution Time
The most recent runtime of this code was recorded as 27 seconds.

## 04_1_FEATURE SELECTION FOR ATTACK FILES

### Description
Feature importance is analyzed specifically for attack files using the Random Forest model. This involves calculating the importance of each feature and visualizing these importances to understand which features are most significant for detecting attacks.

### Execution Time
The most recent runtime of this code was recorded as 61 seconds.

## 04_2_FEATURE SELECTION FOR ALL DATA

### Description
Feature importance is assessed across the entire dataset, including both attack and normal traffic. This analysis helps in identifying the most influential features for overall model performance.

### Execution Time
The most recent runtime of this code was recorded as 306 seconds.

## 05_ACCURACY CALCULATION

### Description
This step assesses the performance of a RandomForestClassifier model for multi-label classification. The dataset is split into training and testing sets, with added noise to simulate real-world conditions. The model is trained and evaluated, with accuracy metrics, classification reports, and confusion matrices generated for each label. Class distribution and sample counts are also reported.

### Execution Time
The most recent runtime of this code was recorded as 504 seconds.

## 06_1_MACHINE LEARNING IMPLEMENTATION FOR ATTACK FILES

### Description
Models are trained and evaluated specifically on attack files to assess their performance. This includes calculating and comparing accuracy, precision, recall, and other metrics to determine how well the models detect different attack types.

### Execution Time
The most recent runtime of this code was recorded as 272 seconds.

## 06_2_MACHINE LEARNING IMPLEMENTATION WITH FEATURES

### Description
Machine learning models are trained using a selected set of features from the dataset. This step includes evaluating the models' performance with these features and comparing the results to assess their effectiveness.

### Execution Time
The most recent runtime of this code was recorded as 176 seconds.

## 06_3_MACHINE LEARNING MEASURE COMPARISON

### Description
A comparison of different models based on various performance measures, including accuracy, precision, recall, and AUC, is conducted. This step provides a comprehensive view of how each model performs in terms of detecting anomalies.

### Execution Time
The most recent runtime of this code was recorded as 17 seconds.

## 06_4_FINAL MACHINE LEARNING IMPLEMENTATION

### Description
The final implementation involves training and evaluating the selected machine learning models using the complete dataset. Performance metrics are calculated, and results are analyzed to determine the best model for anomaly detection.

### Execution Time
The most recent runtime of this code was recorded as 556 seconds.

## COMPARISON GRAPHS

### Description
Graphs comparing the performance of different models are generated, including ROC curves and bar plots for accuracy, precision, and recall. These visualizations help in understanding the relative performance of each model.

### Execution Time
The most recent runtime of this code was recorded as 50 seconds.

## HEAT MAP

### Description
Heat maps are used to visualize confusion matrices, providing a clear view of how each model performs in terms of true positives, false positives, true negatives, and false negatives.

### Execution Time
The most recent runtime of this code was recorded as 1 second.

## ACCURACY, PRECISION, RECALL VALUES FOR EACH MODEL

### Description
Performance metrics, including accuracy, precision, and recall, are computed for each model and displayed in tabular and graphical formats. This helps in comparing the effectiveness of different models in detecting anomalies.

### Execution Time
The most recent runtime of this code was recorded as 66 seconds.

## CONFUSION MATRICES

### Description
Confusion matrices for each model are generated to evaluate the performance in classifying different attack types and normal traffic. These matrices provide detailed information on the number of true and false classifications.

### Execution Time
The most recent runtime of this code was recorded as 89 seconds.

## FEATURE IMPORTANCE GRAPH

### Description
The importance of features is visualized using a bar graph, showing how each feature contributes to the performance of the Random Forest model. This helps in identifying key features that influence model predictions.

### Execution Time
The most recent runtime of this code was recorded as 23 seconds.
