# Credit Card Fraud Detection
## Project Overview
This project aims to detect credit card fraud using an imbalanced dataset from Kaggle. I've employed various data engineering techniques using Pandas and evaluated the performance of five different machine learning algorithms: Logistic Regression, Shallow Neural Networks, Random Forest, Gradient Boosting, and Linear Support Vector Machine (Linear SVM). The evaluation metrics include precision, recall, and F1 score. Prior to balancing the dataset, all algorithms were able to successfully classify all non-fraudulent entries.

## Data Engineering
In this section, I'll outline the data engineering steps taken to prepare the dataset for modeling. This includes data preprocessing, handling missing values, feature engineering, and any data transformations.

In this project, I employed extensive data engineering techniques using Pandas and NumPy to prepare the dataset for machine learning. My approach included:

### 1. Normalization: 
I rescaled all numeric features within the dataset to a standardized range, typically between 0 and 1. Normalization helps ensure that all features contribute equally to the model, preventing dominance by variables with larger scales.

### 2. Generalization: 
I conducted feature engineering and generalization by simplifying or aggregating certain features. This not only reduced dimensionality but also enhanced the model's ability to recognize patterns in the data.

### 3. Randomization: 
To eliminate any inherent order or bias in the dataset, I randomized the data, ensuring that the sequence of records would not influence the model's performance.

### 4. Data Split: 
I divided the dataset into distinct subsets for training, testing, and validation. This separation allowed us to train the model on one portion, validate it on another, and assess its generalization performance on a separate unseen dataset.

My data engineering efforts were crucial in preparing the dataset for accurate and effective machine learning model training.



## Algorithms
### 1. Logistic Regression
Logistic Regression is employed in fraud detection due to its interpretability, computational efficiency, and simplicity. Its transparency in revealing the impact of each variable on predictions helps identify potential fraud indicators, while its scalability allows it to handle large datasets effectively. Additionally, Logistic Regression can serve as a useful baseline model for evaluating the performance of more complex algorithms in fraud detection.

### 2. Shallow Neural Networks
Shallow Neural Networks find application in fraud detection due to their capacity to capture complex non-linear relationships and automatically extract pertinent features from data. Their adaptability to changing fraud patterns, ability to handle diverse data types, and suitability for anomaly detection make them a valuable tool for robust and continuous fraud detection. Additionally, their parallel processing capabilities enable efficient handling of large datasets, making them ideal for real-time or high-volume fraud detection systems.

### 3. Random Forest
Random Forest is a favored choice for fraud detection due to its ensemble learning, which combines multiple decision trees to improve accuracy and generalization. It excels at handling imbalanced data, providing insights into feature importance, and minimizing the risk of overfitting. Its versatility, ease of implementation, and the ability to parallelize processing make it a practical and effective tool for accurate fraud detection.

### 4. Gradient Boosting
Gradient Boosting is favored for fraud detection due to its high accuracy, the ability to handle imbalanced data, and the provision of valuable insights into feature importance. Its sequential learning process and versatility with different data types make it a powerful choice for detecting fraudulent activities. Additionally, it's less prone to overfitting, ensuring reliable performance, even with limited data.

### 5. Linear SVM
Linear Support Vector Machine (Linear SVM) is employed in fraud detection for its ability to maximize the margin between classes, enabling effective differentiation between normal and fraudulent transactions. It excels in generalization to unseen data, robustness against outliers, and scalability for large datasets, making it a valuable tool for accurate fraud detection. Additionally, Linear SVM provides transparency in feature importance, aiding in the identification of potential fraud indicators.

## Performance Evaluation
I measured the performance of each algorithm using the following metrics:

* Precision: Precision measures the number of true positive predictions over the total positive predictions.

* Recall: Recall calculates the number of true positive predictions over the total actual positives.

* F1 Score: The F1 score is the harmonic mean of precision and recall, offering a balanced evaluation of the model's performance.

## Results
After extensive evalutation of the five machine learning algorithms, I obeserved the following results:
* Logistic Regression: Precision - [73%], Recall - [53%], F1 Score - [61%]
* Shallow Neural Networks: Precision - [77%], Recall - [75%], F1 Score - [76%]
* Random Forest: Precision - [77%], Recall - [47%], F1 Score - [59%]
* Gradient Boost: Precision - [67%], Recall - [67%], F1 Score - [67%]
* Linear SVM: Precision - [66%], Recall - [75%], F1 Score - [70%]

It's important to note that prior to dataset balancing, the results revealed that the Random Forest and Shallow Neural Networks algorithms boasted the best precision score. Shallow Neural Networks and Linear SVM had the best recall scores, and Shallow Neural Networks outperformed in terms of the F1 score.

However, it's crucial to emphasize that the overall model performance was adversely affected by the severe class imbalance in the dataset. The rarity of fraudulent cases made it challenging for the algorithms to accurately classify them. As a result, all the algorithms' scores, while showing promise in specific areas, were suboptimal.

To see balanced dataset results you can view the metrics.txt file.
