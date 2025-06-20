# 🔥 Distributed Wildfire Confidence Prediction using H2O.ai
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![H2O.ai](https://img.shields.io/badge/H2O.ai-distributed-yellow)
![License: MIT](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/status-active-success)

> A multiclass classification project leveraging a **2-node distributed H2O cluster** and **Random Forest** algorithm to predict wildfire confidence levels with high accuracy.

---

## 📌 Highlights

- 🖥️ **Deployed a 2-node H2O cluster** to distribute training  
- 🌲 Trained a **Distributed Random Forest (DRF)** for **multiclass wildfire confidence prediction**  
- 📈 Achieved **97.75% accuracy** with strong per-class precision and recall  
- 🧪 Includes end-to-end **data preprocessing, training, evaluation, and reporting**  
- 📚 Linked with a detailed PDF **project report** and **cluster setup guide**

---

## 📂 Repository Structure

- 📁 [`Final_Distributed_ML_using_H2O Framework.ipynb`](./Final_Distributed_ML_using_H2O%20Framework.ipynb) — Complete code notebook  
- 📁 [`📊 Project Report: Predictive Modeling using H2O.ai.pdf`](./📊%20Project%20Report_%20Predictive%20Modeling%20using%20H2O.ai.pdf) — Final report  
- 📁 [`README.md`](./README.md) — You're here  
---

## ⚙️ How to Run the Project

> Run this notebook locally using **Jupyter** or **VS Code** with required Python packages.

### 1. Clone this repo
```bash
git clone https://github.com/kananpandit02/wildfire_pred_h2o.git
cd wildfire_pred_h2o
```
### 2. Install dependencies
```bash
pip install h2o pandas numpy matplotlib
```
3. Launch notebook
```bash
jupyter notebook
```
Then open [**Final_Distributed_ML_using_H2O Framework.ipynb**](./Final_Distributed_ML_using_H2O%20Framework.ipynb) and run the cells step-by-step.


---

## 🌐 Distributed H2O Cluster Setup

This project uses **two physical machines** connected on a private network.

- H2O cluster is configured using `flatfile.txt`  
- Each node runs `h2o.jar` with the same cluster name  
- DRF model training is automatically parallelized across both machines

📎 **View Full Cluster Setup Guide**:  
🔗 [kananpandit02/h2o_cluster_setup](https://github.com/kananpandit02/h2o_cluster_setup)



---

## 📦 Dataset

The dataset used in this project contains wildfire records with features such as:

- Latitude & Longitude
- Brightness
- Scan & Track
- Satellite Type
- Fire Radiative Power (FRP)
- Confidence (Target - Multiclass: Low, Medium, High)

It was loaded using `h2o.import_file()` and split into training, validation, and test sets using `H2OFrame.split_frame()`.

> ⚠️ Due to size/licensing, the dataset is not included in this repository. Please contact the author or refer to public wildfire datasets like [NASA FIRMS](https://firms.modaps.eosdis.nasa.gov/) or [Kaggle wildfire datasets](https://www.kaggle.com/datasets) to explore similar data.

---

## 📈 Model Performance

| Metric       | Value   |
|--------------|---------|
| AUC          | 0.948   |
| RMSE         | 0.135   |
| Accuracy     | 97.75%  |
| Precision    | 97.5%   |
| Recall       | 98.0%   |
| F1-score     | 97.7%   |

**Confusion Matrix:**

|            | Actual 0 | Actual 1 |
|------------|----------|----------|
| **Pred 0** |   980    |    20    |
| **Pred 1** |    25    |   975    |

