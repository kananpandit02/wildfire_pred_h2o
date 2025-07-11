# 🔥 Distributed Wildfire Confidence Prediction using H2O.ai

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![H2O.ai](https://img.shields.io/badge/H2O.ai-distributed-yellow)
![License: Academic Use](https://img.shields.io/badge/License-Academic%20Use%20Only-lightgrey)
![Status](https://img.shields.io/badge/status-active-success)

> A multiclass classification project leveraging a **2-node distributed H2O cluster** and a **Distributed Random Forest (DRF)** model to predict wildfire confidence levels using **VIIRS SNPP 2023 global data**.

---

## 📌 Highlights

- 🌍 Used **2023 VIIRS SNPP global wildfire data** from NASA FIRMS  
- 🖥️ Deployed a **2-node H2O cluster** for distributed model training  
- 🌲 Trained a **Distributed Random Forest (DRF)** for **multiclass classification**  
- 📈 Achieved **97.75% accuracy**, AUC of **0.948**  
- 🧪 Includes full **data preprocessing, training, evaluation, and export**  
- 📚 Linked with a detailed PDF **project report** and **cluster setup guide**  

---

## 📂 Repository Structure

```plaintext
wildfire_pred_h2o/
├── Final_Distributed_ML_using_H2O Framework.ipynb   # Main notebook
├── 📊 Project Report: Predictive Modeling using H2O.ai.pdf  # Final report
├── flatfile.txt                                     # H2O node list for cluster
├── requirements.txt                                 # Python dependencies
├── README.md                                        # This file

```
## ⚙️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/kananpandit02/wildfire_pred_h2o.git  
cd wildfire_pred_h2o
```
### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
### 3. Launch the Notebook
```bash
jupyter notebook
```
Then open Final_Distributed_ML_using_H2O_Framework.ipynb and run the cells step-by-step.
### 🌐 Distributed H2O Cluster Setup
This project utilizes two physical machines on a private network to build a distributed H2O cluster.

## ⚙️ Setup Steps:
Ensure both machines are connected to the same network.

Create a flatfile.txt that lists the IP addresses of each node, e.g.:
```bash

192.168.0.101
192.168.0.102
```
On each machine, run the following command:
```bash

java -Xmx4g -jar h2o.jar -name wildfire-cluster -flatfile flatfile.txt
```
## 📎 Full Cluster setup guide available at:
[kananpandit02/h2o_cluster_setup](https://github.com/kananpandit02/h2o_cluster_setup)
