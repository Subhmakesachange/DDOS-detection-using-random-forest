# README

## DDoS Defense: A Multiclass and Multidimensional Detection System with Diverse Machine Learning Models

This project focuses on building a system to detect and classify **DDoS (Distributed Denial of Service)** attacks using the **CICDDoS2019** dataset. The primary goal is to develop a multiclass classification model capable of identifying various DDoS attack types alongside normal network traffic.

### Dataset

The **CICDDoS2019** dataset contains network traffic data with several types of DDoS attacks and benign traffic. Key attributes include packet size, source/destination IPs, and protocol types. The target variable includes labels such as Syn, Benign, Portmap, UDP, UDPLag, MSSQL, NetBIOS, and LDAP.

### Process Overview

1.  **Data Collection and Preprocessing**:
    *   Collected training and testing dataset paths.
    *   Ensured consistent column names between training and testing sets.
    *   Handled null values (none found) and removed duplicate rows.
    *   Dropped columns with single unique values and highly correlated columns (correlation >= 0.8).
2.  **Exploratory Data Analysis (EDA)**:
    *   Visualized the distribution of categorical and numerical columns.
    *   Analyzed flow duration and packet length mean by protocol and attack label.
    *   Examined packet flag distributions and protocol request counts.
    *   Generated a correlation matrix to understand feature relationships.
3.  **Data Preprocessing and Feature Engineering**:
    *   Split the data into training, validation, and test sets.
    *   Encoded the target variable using LabelEncoder.
    *   Applied MinMaxScaler for feature scaling.
4.  **Model Training and Evaluation**:
    *   Trained and evaluated several models: Random Forest, KNN, Extra Trees, MLP Classifier, and XGBoost.
    *   Evaluated models using accuracy, precision, recall, F1-score, and ROC AUC.
    *   Visualized ROC curves for multiclass classification.
    *   Displayed a table comparing model scores.
5.  **Results Visualization**:
    *   Plotted accuracy scores for visual model comparison.
    *   Visualized ROC curves for all models.

### Results and Recommendation

Based on the evaluation metrics, the **Random Forest** model demonstrated balanced performance across all metrics, making it the recommended choice for DDoS prediction. The **MLP Classifier** also showed potential, particularly in distinguishing between DDoS and non-DDoS traffic.

### Conclusion

This project successfully evaluated various machine learning models for DDoS attack detection using the CICDDoS2019 dataset, providing insights into their effectiveness for classifying different attack types and contributing to the development of more robust cybersecurity systems.

For more details on the dataset, visit the [CICDDoS2019 Dataset Page](https://www.unb.ca/cic/datasets/ddos-2019.html).
