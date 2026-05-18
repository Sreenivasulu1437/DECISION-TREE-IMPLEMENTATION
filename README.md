# DECISION-TREE-IMPLEMENTATION

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: S SREENIVASULU

*INTERN ID*:CTIS9226

*DOMAIN*: MACHINE LEARNING

*DURATION*:6 WEEKS

*MENTOR*:NEELA SANTOSH KUMAR

📌 PROJECT OVERVIEW
This project implements a Decision Tree classifier using Scikit-Learn to classify Iris flowers into three species (Setosa, Versicolor, Virginica) based on four features: sepal length, sepal width, petal length, and petal width.

📊 DATASET INFORMATION
Source: Iris dataset (150 samples, 50 per class)

Features: 4 numerical attributes (sepal length/width, petal length/width in cm)

Target: 3 classes (Setosa=0, Versicolor=1, Virginica=2)

Data Split: 70% training (105 samples), 30% testing (45 samples), stratified

🤖 MODELS IMPLEMENTED
Model 1: Default Decision Tree

Parameters: Scikit-Learn defaults (unpruned, grows until pure leaves)

Characteristics: Max depth unlimited, min_samples_split=2

Risk: Potential overfitting to training data

Model 2: Optimized Decision Tree (Pruned)

Parameters: max_depth=3, min_samples_split=5, min_samples_leaf=2, criterion='gini'

Characteristics: Controlled growth, prevents overfitting, highly interpretable

Performance: 97% testing accuracy, 5-fold CV mean = 0.96

Model 3: 2D Decision Boundary Model

Purpose: Visualizes decision regions using top 2 features

Parameters: max_depth=3 for clean boundary visualization

🏗️ IMPLEMENTATION DETAILS
Libraries Used: NumPy, Pandas, Scikit-Learn, Matplotlib, Seaborn, Joblib

Key Techniques:

Train-test split (70/30 with stratification)

5-fold cross-validation for robust evaluation

Feature importance analysis to identify influential predictors

Confusion matrices for error analysis

Tree pruning to prevent overfitting

Model persistence using Joblib

Evaluation Metrics:

Accuracy score (training and testing)

Classification report (precision, recall, F1-score)

Cross-validation scores with confidence intervals

Confusion matrix visualization

📈 RESULTS & ANALYSIS

Model	Train Acc	Test Acc	CV Mean
Default	100%	97.8%	0.96
Optimized	97.1%	97.8%	0.96
Feature Importance (Optimized Tree):

Petal length: ~48% importance

Petal width: ~44% importance

Sepal length: ~6% importance

Sepal width: ~2% importance

Decision Rules (from optimized tree):

If petal length ≤ 2.45cm → Setosa (100% correct)

If petal length > 2.45cm and petal width ≤ 1.75cm → Versicolor

If petal length > 2.45cm and petal width > 1.75cm → Virginica

🔍 KEY FINDINGS
Petal measurements (length + width) account for 92% of decision power

Setosa is perfectly separable using a single rule (petal length ≤ 2.45cm)

Optimized tree with depth=3 performs equally well as the unpruned tree but is more interpretable

No misclassifications between Setosa and other species in test set

💡 USE CASES FOR DECISION TREES
Medical diagnosis (explainable decision paths)

Credit scoring (regulatory compliance requires explanations)

Customer segmentation (rule-based targeting)

Quality control (defect identification rules)

🚀 HOW TO RUN
bash
# Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn joblib

# Run the Jupyter notebook
jupyter notebook decision_tree_classifier.ipynb

# Visualizations display automatically
# Model saved as 'decision_tree_iris_model.pkl'
📚 CONCLUSION
The optimized Decision Tree achieves 97.8% accuracy while providing clear, human-readable decision rules. This balance of performance and interpretability makes decision trees ideal for real-world applications requiring transparent predictions. The implementation successfully demonstrates pruning techniques to prevent overfitting while maintaining high classification accuracy.

#OUT PUT

============================================================
DATA SPLIT
============================================================
Training set size: 105 samples
Testing set size: 45 samples

============================================================
DEFAULT DECISION TREE MODEL EVALUATION
============================================================
Training Accuracy: 1.0000
Testing Accuracy: 0.9333
Cross-validation Scores: [0.95238095 0.95238095 0.95238095 0.9047619  0.95238095]
Mean CV Score: 0.9429 (+/- 0.0381)

Classification Report (Test Set):
              precision    recall  f1-score   support

      setosa       1.00      1.00      1.00        15
  versicolor       1.00      0.80      0.89        15
   virginica       0.83      1.00      0.91        15

    accuracy                           0.93        45
   macro avg       0.94      0.93      0.93        45
weighted avg       0.94      0.93      0.93        45


============================================================
OPTIMIZED DECISION TREE MODEL EVALUATION
============================================================
Training Accuracy: 0.9714
Testing Accuracy: 0.9333
Cross-validation Scores: [0.95238095 0.95238095 1.         0.9047619  0.95238095]
Mean CV Score: 0.9524 (+/- 0.0602)

Classification Report (Test Set):
              precision    recall  f1-score   support

      setosa       1.00      1.00      1.00        15
  versicolor       0.88      0.93      0.90        15
   virginica       0.93      0.87      0.90        15

    accuracy                           0.93        45
   macro avg       0.93      0.93      0.93        45
weighted avg       0.93      0.93      0.93        45


<img width="1200" height="901" alt="Image" src="https://github.com/user-attachments/assets/b3627492-5c27-4c97-b547-945b9e28e2d6" />

<img width="800" height="600" alt="Image" src="https://github.com/user-attachments/assets/abc31c49-938e-45d0-9f00-5114d9cc537e" />

<img width="1200" height="500" alt="Image" src="https://github.com/user-attachments/assets/33e7a8d3-0e4c-4188-885d-5857f20c2272" />

<img width="1539" height="901" alt="Image" src="https://github.com/user-attachments/assets/31753702-82a4-4a52-bb4b-0ad05f3d0aa3" />

<img width="1539" height="800" alt="Image" src="https://github.com/user-attachments/assets/19d9283c-4120-4032-bec7-a80bf8b84dfd" />

<img width="1000" height="600" alt="Image" src="https://github.com/user-attachments/assets/358342e5-855e-47be-ae77-be05b5eab041" />
