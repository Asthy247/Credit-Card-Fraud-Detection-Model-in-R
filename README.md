# Credit-Card-Fraud-Detection-Model-in-R

# Introduction

Credit card fraud has become a significant concern for financial institutions and individuals alike. 

With the increasing prevalence of online transactions, fraudulent activities have also surged. 

This project aims to develop a robust model to detect fraudulent credit card transactions, leveraging machine learning techniques and data analysis.


**Why is it vital?**


Credit card fraud poses significant financial risks to both individuals and businesses. **Here's why it's crucial:**

**Financial Loss:** Fraudulent transactions can result in direct financial losses for individuals and businesses.

**Damaged Reputation:** For businesses, fraud can damage their reputation and erode customer trust.

**Increased Costs:** Financial institutions and businesses incur costs associated with fraud prevention, investigation, and chargebacks.
	
**Regulatory Compliance:** Many industries have strict regulations regarding fraud prevention and detection. Failure to comply can lead to hefty fines.



**Methods of Detection:**


**Several techniques are employed to detect fraud:**

**•Rule-based systems**:** These systems use predefined rules to flag suspicious transactions.

• **Statistical analysis:**** Statistical methods can identify anomalies in transaction patterns.
**
**•	Machine learning**: Advanced machine learning algorithms can analyze vast amounts of data to detect complex patterns and anomalies.

**•	Biometric authentication:** Techniques like fingerprint and facial recognition can verify the identity of the cardholder.



# Data Understanding and Preparation


# Data Exploration:


# Dataset: 

We utilized a dataset containing a large number of credit card transactions, each characterized by various features.


**20000 rows:** This means there are 20,000 observations or data points in the dataset. 

**31 columns:** This indicates that each observation has 31 features or variables associated with it.

The Class column was converted in the credit card data frame. Since, it involves classification, and for the categorical variables to be in factor format.


**Class Imbalance:** The dataset exhibited a significant class imbalance, with a disproportionately large number of legitimate transactions compared to fraudulent ones.

We checked the missing value and it is **zero**.


# Descriptive Statistics of the Dataset

•	**Min**: Minimum value

•	**1st Qu.**: First quartile (25th percentile)

•**Median:** Median (50th percentile)

**•	Mean:** Mean (average)

**•	3rd Qu.:** Third quartile (75th percentile)

**•	Max:** Maximum value



**Frequency Table for the Class Column in the Credit Card Dataset**

![image](https://github.com/user-attachments/assets/d0420034-5571-43e3-b144-69d93899c258)

 **19936:** This number represents the count of legitimate transactions (class 0). 
 
***64:**** This number represents the count of fraudulent transactions (class 1).



****Percentage of Fraudulent and Legitimate Transactions in the Credit Card data**


![image](https://github.com/user-attachments/assets/a446fb14-ee98-47b9-a5d6-72a33497d0f0)

**0.9968:** This represents approximately 99.68% of the transactions are legitimate (class 0). 

**0.0032:** This represents approximately 0.32% of the transactions are fraudulent (class 1)



# Pie Chart Visualization for Credit Card Transactions

![image](https://github.com/user-attachments/assets/83bf0ebb-30fa-48b4-b964-c2c35127944d)

The pie chart visually represents the distribution of legitimate and fraudulent transactions in the dataset.


**Key Observations:**

**•	Dominance of Legitimate Transactions:** The large orange slice represents legitimate transactions, which account for approximately 99.68% of the total transactions.

**•	Small Fraction of Fraudulent Transactions:** The tiny red slice represents fraudulent transactions, which constitute only 0.32% of the total transactions.



# Confusion Matrix

![image](https://github.com/user-attachments/assets/7653fc1a-0f4c-43e3-9760-1fd226e15056)

**Analyzing the Confusion Matrix**

The confusion matrix provides a detailed breakdown of the model's performance in classifying credit card transactions as legitimate (0) or fraudulent (1).

**Breakdown of the Matrix:**

****•	True Positives (TP):** **19936 - The model correctly predicted 19936 legitimate transactions as legitimate.

******•	False Positives (FP)****: 0 - The model incorrectly predicted 0 legitimate transactions as fraudulent.

**•	False Negatives (FN):** 64 - The model incorrectly predicted 64 fraudulent transactions as legitimate.

**•	True Negatives (TN)**: 0 - The model correctly predicted 0 fraudulent transactions as fraudulent.



**Key Metrics and Their Interpretation:**

**•Accuracy:** 0.9968

o	Overall accuracy, calculated as (TP+TN) / (TP+FP+FN+TN). It shows that the model is highly accurate in predicting legitimate transactions.

**•	Sensitivity (Recall)**: 1.0000

o	The model correctly identifies all legitimate transactions (true positives).

**•	Specificity**: 0.0000

o	The model fails to correctly identify any fraudulent transactions (false negatives).

**•	Precision:** 0.9968

o	Of all the transactions predicted as legitimate, 99.68% are actually legitimate.

**•	F1-Score**: Not shown, but it would be low due to the high number of false negatives.


# Scatter Plot Visualization between two Features (V1 & V2)

![image](https://github.com/user-attachments/assets/bca70282-e3d4-492f-96cc-ccef29ff8542)

The scatter plot you provided is a visualization of the relationship between two features (V1 and V2) in the credit card dataset,

with the color of the points representing the class (fraudulent or legitimate).

**Observations:**

**•	Cluster Separation**: The plot shows a clear separation between the two classes. 

The majority of legitimate transactions are clustered together, while fraudulent transactions form a distinct cluster.

**•	Outliers**: There are some outliers in both classes, particularly in the legitimate class, which might be due to unusual transaction patterns.

**•	Imbalanced Classes:** The plot visually confirms the class imbalance, with a significantly larger number of legitimate transactions compared to fraudulent ones.


# Machine Learning Model for Credit Card

The credit card dataset was split into training and testing sets.

The output confirms that the training set has 1600 rows and 31 columns, while the testing set has 400 rows and 31 columns.

**Purpose:**

**•	Model Training**: The training set is used to train a machine learning model on the historical data.

**•	Model Evaluation:** The testing set is used to evaluate the performance of the trained model on unseen data.

By splitting the data into training and testing sets, we ensure that the model is not overfitted to the training data and can generalize well to new, unseen data.

![image](https://github.com/user-attachments/assets/7619808a-2fbe-48bf-bbc5-44e5df9a75c9)


# Scatter Plot Visualization between two Features (V1 & V2)

![image](https://github.com/user-attachments/assets/a8387bb9-9171-4a57-8edf-1d3a64a03e31)

**Observations:**

**•	Cluster Separation**: The plot shows a clear separation between the two classes.

The majority of legitimate transactions are clustered together, while fraudulent transactions form a distinct cluster.

**•	Outliers:** There are some outliers in both classes, particularly in the legitimate class, which might be due to unusual transaction patterns.

****•	Imbalanced Classes**: The plot visually confirms the class imbalance, with a significantly larger number of legitimate transactions compared to fraudulent ones.


# Understanding Oversampling and Its Impact

Oversampling is a technique used to address class imbalance in datasets, where one class (often the minority class) 

has significantly fewer instances than the other. 

In the context of credit card fraud detection, fraudulent transactions are typically a minority class

![image](https://github.com/user-attachments/assets/d2d3ba08-985f-4eae-9e35-b14b3ed775e8)

•	The original dataset likely had a significant imbalance, with many more legitimate transactions (class 0) than fraudulent ones.

•	After oversampling, the number of fraudulent transactions (class 1) has been significantly increased, bringing the class distribution closer to balance

**Why Oversampling?**

**•	Improved Model Performance**: Imbalanced datasets can lead to biased models that are good at predicting the majority 

class but poor at predicting the minority class. Oversampling helps to address this issue by providing more training examples for the minority class.


**•	Better Detection of Fraudulent Transactions:** By increasing the number of fraudulent transactions in the training data,

the model can learn to identify patterns associated with fraud more effectively.

# Scatter Plot Visualization between two Features (V1 & V2)

![image](https://github.com/user-attachments/assets/b0e42382-1330-4690-874d-912382420c25)

****Observations:**

**•	Cluster Separation:** The plot shows a clear separation between the two classes. 

The majority of legitimate transactions are clustered together, while fraudulent transactions form a distinct cluster.

****•	Outliers**:There are some outliers in both classes, particularly in the legitimate class, which might be due to unusual transaction patterns.

**•	Imbalanced Classes**: The plot visually confirms the class imbalance, with a significantly larger number of legitimate transactions compared to fraudulent on.

# Understanding Undersampling

Undersampling is a technique used to address class imbalance in datasets, where one class (often the majority class) 

has significantly more instances than the other. In the context of credit card fraud detection, legitimate transactions are typically the majority class.

![image](https://github.com/user-attachments/assets/eeebfdba-9776-4ef0-8d58-ceed83b75d34)

•	The original dataset likely had a significant imbalance, with many more legitimate transactions (class 0) than fraudulent ones.

•	After undersampling, the number of legitimate transactions (class 0) has been reduced, bringing the class distribution closer to balance.

**Why Undersampling?**

**•	Improved Model Performance:** Imbalanced datasets can lead to biased models that are good at 

predicting the majority class but poor at predicting the minority class. 

Undersampling helps to address this issue by reducing the number of instances in the majority class.

**•	Faster Training:** With a smaller dataset, training time can be reduced.


# Scatter Plot Visualization between two Features (V1 & V2)

![image](https://github.com/user-attachments/assets/6f4b4044-1cb4-48f8-94d0-0f6368fff00f)

**Key Observations:**

**•	Cluster Separation**: The plot shows a clear separation between the two classes.

The majority of legitimate transactions are clustered together, while fraudulent transactions form distinct clusters.

**•	Outliers**: There are some outliers in both classes, particularly in the legitimate class, which might be due to unusual transaction patterns.

**•	Class Imbalance:** The plot visually confirms the class imbalance, with a significantly larger number of legitimate transactions compared to fraudulent ones.


# Analyzing the Class Distribution in the Sampled Dataset

![image](https://github.com/user-attachments/assets/c23e2b00-02ff-4d12-ab05-45bd3b954dc8)

This means there are 817 instances of class 0 (legitimate transactions) and 783 instances of class 1 (fraudulent transactions) in the sampled dataset.

This means that approximately 51% of the sampled transactions are legitimate, and 49% are fraudulent.


# Scatter Plot Visualization between two Features (V1 & V2)

![image](https://github.com/user-attachments/assets/8207e9cc-9b3e-4613-8f47-f82f61d2a7ee)

**Observations:**

**•	Cluster Separation:** The plot shows a clear separation between the two classes.

The majority of legitimate transactions are clustered together, while fraudulent transactions form distinct clusters.

**•	Outliers:** There are some outliers in both classes, particularly in the legitimate class, which might be due to unusual transaction patterns.

**•	Imbalanced Classes:** The plot visually confirms the class imbalance, with a significantly larger number of legitimate transactions compared to fraudulent ones.

# Decision Tree (type of supervised learning algorithm) for Credit Card Fraud Detection

![image](https://github.com/user-attachments/assets/2d249570-72cf-4214-a886-9754b7b3f819)

**How to Interpret the Decision Tree:**

**Root Node:** This is the starting point of the tree. Here, the model checks the value of feature V14.

**Internal Nodes:** These nodes represent decision points based on the value of a specific feature.

For example, if V14 is greater than or equal to -0.084, the model moves to the left branch. Otherwise, it moves to the right branch.
	
**Leaf Nodes:** These are the final nodes of the tree and represent the predicted class. In this case, the classes are 0 (legitimate) and 1 (fraudulent).

# Confusion Matrix

![image](https://github.com/user-attachments/assets/1b107e6e-9f7b-489b-bfc6-f7078f8a9651)

**Key Metrics and Interpretation:**


**Accuracy:** 0.99

o	This indicates that the model correctly predicted 99% of the transactions. However, it's crucial to consider other metrics as well, given the class imbalance.



S**ensitivity (Recall):** 0.9950

o	The model correctly identified 99.5% of legitimate transactions. This is a good performance for the majority class.



**Specificity:** 0.0000

o	The model failed to correctly identify any fraudulent transactions. This is a significant issue and highlights the model's inability to detect fraud.



**Precision**: 0.9950

o	Of all the transactions predicted as legitimate, 99.5% were actually legitimate. However, this doesn't capture the model's ability to identify fraudulent transactions.

**F1-Score:** Not shown, but it would be low due to the high number of false negatives.

# Confusion Matrix

![image](https://github.com/user-attachments/assets/ca5b2a30-8641-4d4b-baae-d26490ceb247)

**Key Metrics and Interpretation:**

**Accuracy:** 0.995

o	This indicates that the model correctly predicted 99.5% of the transactions. However, it's crucial to consider other metrics as well, given the class imbalance.



**Sensitivity (Recall):** 1.0000

o	The model correctly identified 100% of legitimate transactions. This is a good performance for the majority class.



**Specificity:** 0.0000

o	The model failed to correctly identify any fraudulent transactions. This is a significant issue and highlights the model's inability to detect fraud.



**Precision:** 0.9950

o	Of all the transactions predicted as legitimate, 99.5% were actually legitimate. However, this doesn't capture the model's ability to identify fraudulent transactions.



**F1-Score**: Not shown, but it would be low due to the high number of false negatives.


# Confusion Matrix

![image](https://github.com/user-attachments/assets/844eda4d-c2b4-4b80-b006-7e207220b9fe)

**Key Metrics and Interpretation:**


**Accuracy**: 0.996

o	This indicates that the model correctly predicted 99.6% of the transactions. However, it's crucial to consider other metrics as well, given the class imbalance.



**Sensitivity (Recall):** 1.0000

o	The model correctly identified 100% of legitimate transactions. This is a good performance for the majority class.



**Specificity**: 0.0000

o	The model failed to correctly identify any fraudulent transactions. This is a significant issue and highlights the model's inability to detect fraud.



**Precision:** 0.996
o	Of all the transactions predicted as legitimate, 99.6% were actually legitimate. However, this doesn't capture the model's ability to identify fraudulent transactions.


**F1-Score:** Not shown, but it would be low due to the high number of false negatives.

# Results and Analysis

Based on the provided results and visualizations, we can draw the following conclusions:

**•	Class Imbalance:** The dataset exhibits a significant class imbalance, with a large number of legitimate transactions and a small number of fraudulent transactions.

**•	Model Performance:** The model's performance, as measured by accuracy and precision, is generally high. 

However, the model struggles to accurately identify fraudulent transactions, as evidenced by the low specificity and high false negative rate.

**•	Feature Importance**: The scatter plots suggest that certain features, such as V1 and V2, are highly discriminative in separating fraudulent and legitimate transactions.

# Recommendations

To improve the model's performance in detecting fraudulent transactions, we recommend the following:

**Address Class Imbalance:** 
o	**Oversampling**: Generate synthetic minority class samples.

**o	Undersampling**: Randomly remove samples from the majority class.

**oClass Weighting: **Assign higher weights to the minority class during training.

**Ensemble Methods:** Combine multiple models to improve overall performance and reduce bias.

**Feature Engineering:** Explore creating new features or transforming existing ones to better capture patterns associated with fraud.

**Hyperparameter Tuning:** Optimize the model's hyperparameters to improve its performance.

**Model Selection:** Evaluate the performance of different machine learning algorithms, considering their suitability for imbalanced datasets.

**Continuous Monitoring and Retraining:** Implement a system to monitor the model's performance over time and retrain it as needed to adapt to evolving fraud patterns.

# Conclusion
In conclusion, credit card fraud detection is a complex task that requires careful consideration of various factors. 

By leveraging machine learning techniques and addressing the inherent challenges of class imbalance, we can develop robust models to effectively identify fraudulent transactions.

**Key findings and recommendations from this project include:**


**•	Model Performance**: While the model exhibits high accuracy in predicting legitimate transactions, it struggles to detect fraudulent ones.

**•	Feature Importance:** Certain features, such as V1 and V2, play a crucial role in distinguishing between fraudulent and legitimate transactions.

**•	Model Improvement:** To enhance the model's performance, strategies such as oversampling, undersampling, 

class weighting, and ensemble methods can be employed. Additionally, exploring more advanced techniques like deep learning or anomaly detection may yield further improvements.

By continuously monitoring the model's performance and retraining it with updated data, we can adapt to evolving fraud patterns and maintain a high level of protection against financial losses.


