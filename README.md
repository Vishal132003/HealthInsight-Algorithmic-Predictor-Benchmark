# Diabetes Prediction Model Comparison

## Project Description
This project compares the performance and stability of three machine learning classification algorithms—K-Nearest Neighbors (KNN), Gaussian Naive Bayes, and Logistic Regression—for predicting diabetes using diagnostic medical data.

The main objective is to evaluate how each model's accuracy changes when different `random_state` values are used during the train-test split. This helps analyze the robustness and reliability of each model.

---

## Dataset
The project uses the `diabetes.csv` dataset.

### Dataset contains:
- Several medical diagnostic features such as:
  - Pregnancies
  - Glucose
  - BloodPressure
  - SkinThickness
  - Insulin
  - BMI
  - DiabetesPedigreeFunction
  - Age
- Target variable:
  - Outcome (0 = No Diabetes, 1 = Diabetes)

---

## Machine Learning Models Used

### 1. K-Nearest Neighbors (KNN)
- Type: Non-parametric algorithm
- Learning type: Lazy learning
- Used for classification based on nearest neighbors
- Sensitive to data split

### 2. Gaussian Naive Bayes
- Type: Probabilistic classifier
- Based on Bayes' Theorem
- Assumes features follow normal distribution
- Faster and moderately stable

### 3. Logistic Regression
- Type: Linear classification algorithm
- Used for binary classification
- Provides probability-based output
- Most stable among all models

---

## Project Workflow

### 1. Data Loading and Preprocessing
- Load diabetes.csv dataset
- Separate features (X) and target variable (y)
- Split dataset into:
  - Training set (80%)
  - Testing set (20%)

---

### 2. Model Training
Initialize and train:

- KNN Classifier
- Gaussian Naive Bayes
- Logistic Regression

Each model is trained using the training dataset.

---

### 3. Initial Performance Evaluation
- Calculate accuracy score for each model
- Use fixed random_state
- Compare initial performance

---

### 4. Random State Stability Analysis
To evaluate robustness:

- Train each model 100 times
- Use random_state values from 0 to 99
- Store accuracy score for each iteration
- Analyze performance variation

---

### 5. Visualization
Line plots are generated to show:

- Random State (X-axis)
- Accuracy (Y-axis)

Separate lines for:

- KNN
- Naive Bayes
- Logistic Regression

This helps visualize stability and performance variation.

---

## Results and Key Findings

### KNN Model
- Showed highest fluctuation in accuracy
- Highly sensitive to train-test split
- Less stable

### Naive Bayes Model
- Moderate stability
- Less fluctuation than KNN
- Good performance

### Logistic Regression Model
- Most stable model
- Highest overall accuracy
- Least sensitive to random_state changes
- Most reliable classifier

---

## Conclusion
This project demonstrates that model performance can vary significantly depending on how the data is split.

Key conclusions:

- Logistic Regression is the most stable and reliable model
- KNN is highly sensitive to data splitting
- Naive Bayes provides balanced performance
- Evaluating models across multiple random states gives better performance estimation

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## How to Run

```bash
pip install numpy pandas scikit-learn matplotlib
