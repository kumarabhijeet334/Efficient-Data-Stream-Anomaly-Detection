# Efficient-Data-Stream-Anomaly-Detection
This Python script implements an efficient algorithm for detecting anomalies in continuous data streams. The simulated data stream represents real-time sequences of floating-point numbers, applicable to various metrics such as financial transactions and system metrics. 
Objectives
Algorithm Selection
Choose an algorithm capable of handling concept drift and seasonality for effective anomaly detection in dynamic data streams.

Data Stream Simulation
Implement a function to simulate a data stream, incorporating a pattern, seasonal component, and noise to replicate real-world scenarios.

Anomaly Detection
Develop a real-time anomaly detection mechanism that flags anomalies as the data stream is being processed.

Optimization
Ensure the algorithm is optimized for speed and efficiency, considering the continuous nature of data streaming.

Visualization
Provide a simple real-time visualization of the data stream, highlighting detected anomalies for easy interpretation.


Random Forest Algorithm:
Random Forest is an ensemble learning method that builds multiple decision trees by using bootstrapped samples and random feature selection.
It combines their predictions through voting (classification) or averaging (regression).
Efficiency:
1. Complex Patterns: Captures complex relationships.
2. Reducing Overfitting: Less prone to overfitting.
3. Feature Selection: Implicitly selects relevant features.
4. Parallelization: Efficient for large datasets.
5. Robustness: Robust to noisy data and outliers.
6. Handling Missing Values: Can handle missing values without imputation.
Time Complexity: O(m⋅log(n))×number of trees


In the dataset, which records credit card transactions over two days in September 2013,
there are a total of 284,807 transactions, out of which 492 are identified as fraudulent.
The imbalance in the dataset is pronounced, with fraudulent transactions accounting for only 0.172% of the total.

Used the dataset of credit cards to recognize fraudulent credit card transactions. The dataset contains transactions made by credit cards in September 2013 by European cardholders.
DATASET LINK: https://drive.google.com/drive/folders/1_nOeY7FkK7FuAe5b9myX49Rt3Yofyp94


Isolation Forest:

Accuracy Score: 98.99%
Precision-Recall Trade-off: While achieving high overall accuracy, the Isolation Forest struggles to correctly identify instances of the positive class (fraudulent transactions). The precision, recall, and F1-score for the positive class (1) are extremely low, indicating that the model fails to effectively capture the fraudulent cases.

Local Outlier Factor (LOF):

Accuracy Score: 100%
Effective Anomaly Detection: LOF demonstrates excellent accuracy, achieving a perfect score. It successfully identifies both normal and fraudulent transactions with precision, recall, and F1-score all equal to 1.

Support Vector Machine (SVM):

Accuracy Score: 36.68%
Challenges with Imbalanced Data: SVM struggles significantly with the imbalanced nature of the dataset. While achieving high recall for the positive class, the precision is extremely low. The model is biased toward classifying transactions as fraudulent, resulting in a compromised overall accuracy.

Conclusion:

Isolation Forest: Performs well in terms of overall accuracy but struggles with detecting fraudulent transactions, resulting in low precision and recall for the positive class.

Local Outlier Factor (LOF): Emerges as the most effective model, achieving perfect accuracy and successfully identifying both normal and fraudulent transactions.

Support Vector Machine (SVM): Faces challenges due to imbalanced data, leading to compromised precision and overall accuracy. The model tends to overpredict the positive class.
