# IoT Network Anomaly Detection Model

## Project Overview
This project focuses on identifying malicious network traffic in IoT devices, specifically targeting Mirai botnet attacks on smart security cameras. By establishing a baseline of normal network behavior, we engineered an end-to-end machine learning pipeline to detect anomalous traffic spikes that indicate a compromised device or a distributed denial-of-service (DDoS) flood. 

This project was developed for ECE 16: Data Science for Engineering Applications at the University of California, Riverside.

## Dataset
*   **Source:** N-BaIoT Dataset via the UCI Machine Learning Repository.
*   **Scale:** Processed a targeted subset of approximately 100,000 tabular, time-series network traffic samples.
*   **Focus:** 115 continuous statistical features mapping the operations of Provision PTZ Security Cameras.

## Tech Stack
*   **Data Processing:** Python, Pandas, NumPy, OS, Glob.
*   **Signal Processing & Visualization:** SciPy (FFT, kurtosis), Matplotlib, Seaborn.
*   **Machine Learning:** Scikit-learn (K-Means++, KNN, StandardScaler), TensorFlow/Keras (CNN, LSTM).

## Methodology & Models
*   **Data Preprocessing:** Standardized all 115 numerical inputs using StandardScaler to force means to 0.0, ensuring massive packet variances did not overpower distance-based algorithms.
*   **Visualizing Threats:** Utilized Fast Fourier Transforms (FFT) and scatter plots to physically map the threat, proving that Mirai attacks cluster tightly by spamming tiny, identical packets with near-zero frequency-domain energy.
*   **Unsupervised Baseline:** Deployed K-Means++ clustering without target labels to prevent the model from blindly guessing. The model successfully separated the traffic with a dense 0.947 Silhouette Score.
*   **Supervised Classification:** Validated the baseline against advanced networks, including a Convolutional Neural Network (CNN) that converged at 99.68% test accuracy, a K-Nearest Neighbors (KNN) model at 99.75%, and a Long Short-Term Memory (LSTM) time-series model.
*   **Optimization & Dimensionality Reduction:** Executed Exact P-Value hypothesis testing to eliminate the least significant features without performance loss. Applied Principal Component Analysis (PCA) to retain 95% variance, effectively cutting Neural Network training time in half, though sacrificing physical feature interpretability.

## Project Status
*   [x] Phase 1 & 2: Data Cleaning, Feature Scaling, and Exploratory Data Analysis (EDA).
*   [x] Phase 3: Correlation analysis (threshold 0.1), signal processing (FFT), and baseline clustering.
*   [x] Phase 4: Supervised neural network comparative analysis (CNN, KNN, LSTM).
*   [x] Phase 5: Hypothesis testing and dimensionality reduction via PCA.

## Contributors
*   **Jeremie Rubio** (jrubi065@ucr.edu)
*   **Karam Kambo** (kkamb001@ucr.edu)
