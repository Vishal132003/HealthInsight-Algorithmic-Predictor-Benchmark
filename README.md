Diabetes Prediction Model Comparison
Project Description
This project aims to compare the performance and stability of three common machine learning classification algorithms—K-Nearest Neighbors (KNN), Gaussian Naive Bayes, and Logistic Regression—in predicting diabetes based on a given dataset. The analysis focuses on evaluating how each model's accuracy varies when different random states are used during the train-test split, providing insights into their robustness.

Data
The analysis uses the diabetes.csv dataset, which contains various diagnostic measurements and a binary outcome variable indicating the presence or absence of diabetes.

Models Used
K-Nearest Neighbors (KNN): A non-parametric, lazy learning algorithm used for classification.
Gaussian Naive Bayes: A probabilistic classifier based on Bayes' theorem, assuming features are normally distributed.
Logistic Regression: A linear model used for binary classification.
Analysis
Data Loading and Preprocessing: The dataset is loaded, and features (x) and the target variable (y) are separated. The data is split into training and testing sets (80/20 ratio).
Model Initialization and Training: Each of the three models (KNN, Naive Bayes, Logistic Regression) is initialized and trained on the training data.
Initial Performance Evaluation: Accuracy scores for each model are calculated and displayed for a single, fixed random_state.
Random State Variability Analysis: To assess robustness, each model is trained and evaluated 100 times, with a different random_state used for the train-test split in each iteration. The accuracy scores from each iteration are stored.
Visualization: Line plots are generated to visualize the accuracy of each model against the different random_state values, allowing for a direct comparison of their performance fluctuations.
Key Findings
KNN Model: Exhibited the most significant fluctuations in accuracy across different random states, indicating high sensitivity to data partitioning.
Naive Bayes Model: Showed moderate stability, with noticeable but less extreme variations in accuracy compared to KNN.
Logistic Regression: Demonstrated the highest stability and generally achieved the highest accuracy scores, indicating robust performance less sensitive to the specific train-test split.
This analysis highlights the importance of evaluating models across multiple data splits to obtain a reliable estimate of their true performance and understand their inherent stability.
