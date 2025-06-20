# 🔥 Distributed Wildfire Confidence Prediction using H2O.ai

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

