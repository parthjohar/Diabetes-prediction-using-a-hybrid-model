🧠 **Diabetes Prediction using RF-LSTM Stack**

This project presents a hybrid machine learning model combining Random Forest (RF) and Long Short-Term Memory (LSTM) networks to predict diabetes using clinical features from the Pima Indians Diabetes Dataset. The goal is to enhance prediction accuracy by integrating ensemble learning with deep learning.

🧩 **Problem Statement**

Diabetes is a chronic disease that requires timely diagnosis and management. Traditional models often fail to capture non-linear and sequential patterns in clinical data. This model leverages the strengths of both Random Forest (for feature-level learning) and LSTM (for sequential pattern recognition) to deliver more robust predictions.

📊 **Dataset**

The model uses the Pima Indians Diabetes Dataset, a well-known benchmark dataset containing 768 instances and 8 numeric input features related to patient health and medical history:

Pregnancies

Glucose

Blood Pressure

Skin Thickness

Insulin

BMI

Diabetes Pedigree Function

Age

Target: Outcome (0: Non-diabetic, 1: Diabetic)

🧼 **Data Preprocessing**

To ensure high model performance and reliability, the following preprocessing steps were applied:

Class Imbalance Handling: Applied SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset.

Feature Scaling: All features were scaled using MinMaxScaler to normalize input values.

Feature Selection: Used an ensemble approach combining Mutual Information, Lasso Regression, and Random Forest feature importance to rank features. Top features from all three methods were merged to form the final feature set.

Train-Test Split: Performed stratified splitting to preserve class ratios.

🧠 **Model Architecture**

🔁 1. Random Forest
Initially trained on the preprocessed dataset.

Instead of final predictions, the probability outputs from the Random Forest are extracted.

These probability scores are reshaped to form sequential inputs for the LSTM layer.

🔁 2. LSTM Model
Implemented using TensorFlow/Keras.

Takes RF output probabilities as time-series input.

Uses one LSTM layer followed by fully connected layers to perform binary classification.

🔧 Hyperparameter tuning was conducted to optimize model performance using a randomized search strategy over parameters like learning rate, hidden units, batch size, and epochs.

📈 **Evaluation Metrics**

Model performance is measured using the following metrics:

Accuracy

Precision

Recall

F1-Score

AUC-ROC Curve

These metrics provide a comprehensive evaluation of classification effectiveness, especially in imbalanced data scenarios.

✅ **Results**

The RF-LSTM stacked model demonstrated:

Strong predictive performance on the test set.

Higher AUC scores and recall compared to standalone models.

An effective combination of structured feature learning and sequential deep learning.

📫 **Contact**

Connect on [LinkedIn](https://www.linkedin.com/in/parth-johar-14b377261/)
