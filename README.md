# Isolation Forest for Anomaly Detection

## Overview
This project implements **Isolation Forest**, an unsupervised anomaly detection algorithm, to detect machine over heat failures beforehand in industrial machines using the **AI4I 2020 Predictive Maintenance Dataset**.  
It serves as a baseline for detecting rare anomalies.

---

## Dataset
**AI4I 2020 Predictive Maintenance Dataset**  
- Source: [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance)  
- Features: Temperatures, torque, rotational speed, tool wear, and machine type.  
- Target: `Machine failure` (binary classification).

---

## Feature Engineering
- `Temp_Diff` = `Process temperature [K]` − `Air temperature [K]`  
- `Power` = `Torque [Nm]` × `Rotational speed [rpm]`  

Categorical features like `Type` are encoded, and all numerical features are scaled for better model performance.

---

## Method
- **Model**: Isolation Forest with 200 estimators.  
- **Contamination**: Tuned to match the approximate proportion of anomalies in the dataset.  
- **Prediction**: -1 → anomaly (1), 1 → normal (0).  
- **Evaluation**: Confusion matrix, classification report, ROC-AUC score, and anomaly visualization.

## How to run
1. Clone the repository: git clone https://github.com/santhoshkuamares/Isolation-Forest-anomaly-detection.git
2. Install dependencies: pip install -r requirements.txt
3. Run the script:python isolation_forest.py

## Author

Santhosh Kumar Elumalai Srinivasan

Contact:
saisanthosh7092@gmail.com
