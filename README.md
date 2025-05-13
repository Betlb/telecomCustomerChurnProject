# **TELECOM CUSTOMER CHURN PREDICTION PROJECT**

## **PROJECT OVERVIEW**

This project aims to predict customer churn in a telecommunications company using big data and machine learning techniques. A scalable solution was developed by leveraging distributed computing technologies such as Apache Spark and Hadoop.

## **PROJECT OBJECTIVES**

- Identify customers with a high risk of churn  
- Analyze the key factors contributing to customer churn  
- Perform efficient analysis on high-volume datasets using distributed data processing infrastructure  

## **DATASET USED**

- **Source:** [Kaggle - Telecom Churn Dataset](https://www.kaggle.com/datasets/spscientist/telecom-data)  
- **Number of Records:** 3333 customers  
- **Number of Features:** 21  
- **Target Variable:** `Churn` (1 = customer left the service, 0 = customer retained)  

The dataset includes customer demographics, service usage patterns, call statistics, and interactions with customer service.

## **TECHNOLOGIES USED**

- Apache Hadoop – Distributed data storage (HDFS)  
- Apache Spark – Distributed computing engine  
- PySpark – Python API for Apache Spark  
- Spark MLlib – Distributed machine learning library  
- Jupyter Notebook – Analysis environment  
- Oracle VirtualBox + Rocky Linux 8 – Virtual server setup  
- Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`  

## **DATA PROCESSING STEPS**

1. **Data Loading:** Transferring data from HDFS into the Spark environment  
2. **Data Cleaning:** Removing missing values and inconsistent records  
3. **Categorical Transformations:** Converting string-based variables to numeric using `StringIndexer`  
4. **Feature Selection and Transformation:** Removing irrelevant features, vectorizing numeric features with `VectorAssembler`  
5. **Feature Scaling:** Normalizing features using `StandardScaler`  
6. **Data Splitting:** Dividing the dataset into 70% training and 30% testing sets  

## **MACHINE LEARNING MODELS USED**

- **Logistic Regression** – Baseline classification model  
- **Random Forest** – Ensemble learning approach  
- **Gradient Boosted Trees (GBT)** – Advanced model for higher accuracy  
- **CrossValidator** was used for hyperparameter tuning  

## **MODEL PERFORMANCE RESULTS**

| **Model**                  | **Accuracy** | **AUC** | **Precision** | **Recall** | **F1 Score** |
|---------------------------|--------------|---------|---------------|------------|--------------|
| Logistic Regression       | 0.862        | 0.834   | 0.857         | 0.862      | 0.859        |
| Random Forest             | 0.943        | 0.915   | 0.944         | 0.943      | 0.943        |
| Gradient Boosted Trees    | 0.951        | 0.923   | 0.952         | 0.951      | 0.951        |
| **Optimized Random Forest** | **0.958**    | **0.932** | **0.959**     | **0.958**  | **0.958**    |

**The best results were achieved using the optimized Random Forest model.**
