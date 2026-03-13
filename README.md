# Malware Detection Using Machine Learning and Deep Learning

**CMP7239 – Applied Machine Learning Coursework**

## Project Overview

This project applies **Machine Learning (ML)** and **Deep Learning (DL)** techniques to detect malware using a cybersecurity dataset. The goal is to analyse system behaviour features extracted from memory and classify samples as **Benign** or **Malware**.

The project implements and evaluates **six algorithms (4 ML + 2 DL)** and compares their performance using standard evaluation metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.

The implementation is provided in a **Jupyter Notebook** and includes the full machine learning workflow: **data loading, exploratory data analysis, preprocessing, model training, evaluation, and visualisation**.

---

# Dataset

Dataset used in this project:

**Obfuscated-MalMem2022**

### Dataset Characteristics

| Property        | Value                    |
| --------------- | ------------------------ |
| Total Samples   | 58,596                   |
| Total Features  | 56                       |
| Target Variable | Class (Benign / Malware) |
| Data Type       | Numerical                |

The dataset contains features extracted from memory forensic analysis tools that describe system and process behaviour.

Example features include:

* pslist.nproc
* dlllist.ndlls
* handles.nhandles
* ldrmodules.not_in_load
* malfind.ninjections
* svcscan.nservices
* callbacks.ncallbacks

These features help identify suspicious activity associated with malware.

---

# Project Workflow

The project follows a complete **machine learning pipeline**:

1. Dataset Loading
2. Exploratory Data Analysis (EDA)
3. Data Preprocessing
4. Feature Scaling
5. Train-Test Split
6. Machine Learning Model Training
7. Deep Learning Model Training
8. Model Evaluation
9. Performance Comparison

---

# Exploratory Data Analysis

EDA was performed to understand the dataset and detect patterns.

The following visualisations were created:

* Class Distribution
* Feature Distribution Histogram
* Correlation Heatmap

These visualisations help analyse feature relationships and dataset balance.

---

# Data Preprocessing

The following preprocessing steps were applied:

* Checking missing values
* Encoding the target variable using **LabelEncoder**
* Removing non-numeric columns
* Feature scaling using **StandardScaler**
* Splitting dataset into **training (80%) and testing (20%) sets**

These steps ensure that the models receive properly prepared input data.

---

# Machine Learning Models

Four machine learning algorithms were implemented:

| Model                        | Description                                            |
| ---------------------------- | ------------------------------------------------------ |
| Random Forest                | Ensemble learning method using multiple decision trees |
| Decision Tree                | Tree-based classification model                        |
| Support Vector Machine (SVM) | Hyperplane-based classifier                            |
| K-Nearest Neighbors (KNN)    | Distance-based classification method                   |

Hyperparameter tuning was performed using **GridSearchCV** for the Random Forest model.

---

# Deep Learning Models

Two neural network models were implemented using **TensorFlow/Keras**.

### Deep Learning Model 1

Architecture:

Input Layer
→ Dense (64 neurons, ReLU)
→ Dense (32 neurons, ReLU)
→ Output Layer (Sigmoid)

---

### Deep Learning Model 2

Architecture:

Input Layer
→ Dense (128 neurons, ReLU)
→ Dense (64 neurons, ReLU)
→ Dense (32 neurons, ReLU)
→ Output Layer (Sigmoid)

Training configuration:

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Epochs: 10
* Batch Size: 32

---

# Evaluation Metrics

The models were evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC Curve
* AUC Score

These metrics provide a comprehensive evaluation of model performance.

---

# Results

All models achieved high performance on the dataset.

### Model Accuracy Comparison

| Model                 | Accuracy |
| --------------------- | -------- |
| Random Forest         | ~0.9999  |
| Decision Tree         | ~0.9998  |
| SVM                   | ~0.9993  |
| KNN                   | ~0.9995  |
| Deep Learning Model 1 | ~0.9999  |
| Deep Learning Model 2 | ~0.9999  |

ROC curves showed **AUC values close to 1.0**, indicating excellent classification performance.

---

# Visualisations

The notebook generates several visual outputs including:

* Class distribution plot
* Feature distribution histogram
* Correlation heatmap
* Confusion matrices for all models
* ROC curve comparison
* Model accuracy comparison

These visualisations support the analysis and interpretation of the results.

---

# Technologies Used

The project was implemented using Python with the following libraries:

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow
* Keras
* Jupyter Notebook

---

# How to Run the Project

### 1. Clone the repository

```
git clone https://github.com/your-username/malware-detection-ml.git
```

### 2. Install required libraries

```
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

### 3. Launch Jupyter Notebook

```
jupyter notebook
```

### 4. Open the notebook

Open the file:

```
Machine Learning and Deep Learning Techniques.ipynb
```

### 5. Run the notebook

Run all cells sequentially to reproduce the analysis and results.

---

# Project Structure

```
malware-detection-project/
│
├
│── Obfuscated-MalMem2022.csv
│
├── Machine Learning and Deep Learning Techniques.ipynb
│
└── README.md
```

---

# Conclusion

This project demonstrates how machine learning and deep learning techniques can effectively detect malware using memory analysis features. The results show that both traditional ML models and neural networks achieve extremely high accuracy, highlighting the effectiveness of AI-based approaches in cybersecurity applications.

---

# Author

Module: CMP7239 – Applied Machine Learning
University: Birmingham City University
