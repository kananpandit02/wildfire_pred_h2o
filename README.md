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
## 📎 Full Cluster Setup Guide Available At:
[kananpandit02/h2o_cluster_setup](https://github.com/kananpandit02/h2o_cluster_setup)

## 📦 Dataset

This project uses **NASA VIIRS SNPP Active Fire/Hotspot Data (375m, NRT)** for the year **2023**, covering **all countries**.

- **Source**: NASA FIRMS  
- **Satellite**: SNPP (Suomi NPP)  
- **Projection**: WGS84 (Latitude/Longitude)  
- **Format**: CSV  
- **Time Period**: Jan 2023 – Dec 2023  
- **Resolution**: 375 meters  

---

## 🔍 Feature Summary

| Feature     | Description                                |
|-------------|--------------------------------------------|
| `latitude`  | Fire latitude (WGS84)                      |
| `longitude` | Fire longitude (WGS84)                     |
| `brightness`| Brightness of fire detection               |
| `scan`      | Width of the scan footprint                |
| `track`     | Length of the scan footprint               |
| `acq_date`  | Date of fire detection                     |
| `acq_time`  | Time of fire detection (UTC)               |
| `satellite` | SNPP satellite ID                          |
| `confidence`| Confidence level (Low, Nominal, High)      |
| `frp`       | Fire Radiative Power (MW)                  |
| `daynight`  | Day or Night detection                     |
| `version`   | Collection version info                    |

---

⚠️ **Dataset not included in this repository.**

📥 **Download from**:  
👉 [https://firms.modaps.eosdis.nasa.gov/download/](https://firms.modaps.eosdis.nasa.gov/download/)

Select the following options on the page:
- **Product**: VIIRS SNPP 375m  
- **Year**: 2023  
- **Region**: Global

