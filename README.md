# WaferFaultDetection
The inputs of various sensors for different wafers have been provided. In electronics, a wafer (also called a slice or substrate) is a thin slice of semiconductor used for the fabrication of integrated circuits. The goal is to build a machine learning model which predicts whether a wafer needs to be replaced or not(i.e., whether it is working or not) based on the inputs from various sensors.


There are two classes: +1 and -1.

    -1 means that the wafer is in a working condition and it doesn’t need to be replaced.
    +1 means that the wafer is faulty and it needs to be replaced.

![semiconductor-wafer-inspection](https://user-images.githubusercontent.com/76097123/159292194-78f9bc96-2be7-4e76-8aa0-028daa8b70e6.jpg) ![Intel_wafer](https://user-images.githubusercontent.com/76097123/159290987-e34f0992-f0ca-46de-81d4-aade006ee673.gif)

## Data Description
The electronic wafer dataset consist of 592 columns

    1.First column contains wafer id
    2.590 column contains the sensor data
    3.Last column contains the target value labels e.g +1 for defective and -1 for not defective.

Apart from training files, we also require a "schema" file from the client, which contains all the relevant information about the training files such as: Name of the files, Length of Date value in FileName, Length of Time value in FileName, Number of Columns, Name of the Columns, and their datatype.

## Architecture

![img1](https://user-images.githubusercontent.com/76097123/159437449-e1b70734-59ae-452c-968f-18850d04e073.jpg)

**Tech used:)**

- Python
- scikit-learn
- sqlite
- pandas
- numpy
- logger
- kneed ( python library for getting best k value)

**Algorithms used**

- KMeans( for clustering)
- Random Forest Classifier
- XGBoost Classifier

**Accuracy Metric** 

- Silhouette score(clustering)
- AUC Score
