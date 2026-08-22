# IoT-Anomaly-Detection
K-means clustering model to detect Mirai botnet spikes using the N-BaIoT dataset

# IoT Network Anomaly Detection Model

## Project Overview
This project focuses on identifying malicious network traffic in IoT devices, specifically targeting Mirai botnet attacks on smart security cameras. By establishing a baseline of normal network behavior, we are developing an unsupervised machine learning model to detect anomalous traffic spikes that indicate a compromised device.

This project is being developed as part of EE 16: Data Science for Engineering Applications at the University of California, Riverside.

## Dataset
*   **Source:** N-BaIoT Dataset
*   **Scale:** Processing a subset of 100,000+ network traffic samples.
*   **Focus:** Traffic data specific to smart security camera operations.

## Methodology & Tech Stack
*   **Languages & Libraries:** Python, Pandas, Scikit-learn, NumPy.
*   **Data Processing:** Utilized Pandas for extensive data cleaning, exploratory data analysis (EDA), and feature selection.
*   **Machine Learning:** Implementing a K-Means Clustering model to differentiate between normal baseline traffic and botnet attack signatures.
*   **Evaluation Metric:** The dataset is highly imbalanced (a common issue in cybersecurity data). Therefore, model performance is evaluated strictly on **Precision and Recall** to avoid the accuracy paradox.

## Current Project Status
The project is currently in active development. 
*   [x] Phase 1 & 2: Data Cleaning and Exploratory Data Analysis
*   [x] Phase 3: Correlation analysis, feature selection, and baseline model training.
*   [ ] Phase 4: Hyperparameter tuning and dimensionality reduction (PCA).

## Contributors
*   **Jeremie Rubio** 
*   **Karam Kambo**
