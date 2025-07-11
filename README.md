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

This project uses **NASA VIIRS SNPP Active Fire/Hotspot Data (375m, Near Real-Time)** for the **entire year of 2023**, covering **all countries worldwide**.

### 🔗 Official Data Sources

- 🌍 **Global Fire Data Download**: [https://firms.modaps.eosdis.nasa.gov/download/](https://firms.modaps.eosdis.nasa.gov/download/)  
- 🌐 **Country-wise Fire Data Viewer**: [https://firms.modaps.eosdis.nasa.gov/country/](https://firms.modaps.eosdis.nasa.gov/country/)

This dataset includes active fire points detected globally by the **Suomi National Polar-orbiting Partnership (SNPP)** satellite using the **VIIRS sensor at 375m resolution**.

### 📄 Data Overview

- **Satellite**: VIIRS SNPP  
- **Temporal Coverage**: January 1 – December 31, 2023  
- **Spatial Coverage**: 🌍 All countries (global)  
- **Resolution**: 375 meters  
- **Projection**: WGS84 (latitude/longitude)  
- **Format**: CSV (also available as KML, SHP via FIRMS)

---

### 🔍 Feature Summary

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

> ⚠️ **Dataset is not included in this repository** due to size constraints.

📥 **To use the same dataset**:
- Go to: [https://firms.modaps.eosdis.nasa.gov/download/](https://firms.modaps.eosdis.nasa.gov/download/)
- Select:
  - **Sensor**: VIIRS SNPP 375m  
  - **Region**: Global  
  - **Date Range**: 01 Jan 2023 to 31 Dec 2023  
  - Format: CSV


## 📈 Model Performance

| Metric     | Value    |
|------------|----------|
| AUC        | 0.948    |
| RMSE       | 0.135    |
| Accuracy   | 97.75%   |
| Precision  | 97.5%    |
| Recall     | 98.0%    |
| F1-score   | 97.7%    |

---

## 🔢 Confusion Matrix (Example Format)

| Actual \ Pred | Low | Medium | High |
|---------------|-----|--------|------|
| **Low**       | 980 | 10     | 10   |
| **Medium**    | 12  | 975    | 13   |
| **High**      | 10  | 15     | 965  |

---

## 🧩 Future Work

- Add satellite-specific **seasonal features**
- Try **H2O AutoML**, **Deep Learning**, and **XGBoost**
- Apply **Hyperparameter Tuning** via Grid Search
- Deploy using **H2O REST API** or build a **Streamlit UI**
- Add **SHAP** or other feature attribution **visualizations**



## 📜 Data Citation & Disclaimer

**Citation**:  
Cite this dataset as:  
> NASA FIRMS. 2023. *VIIRS 375m Active Fire Data (Suomi NPP)*. NASA FIRMS, LANCE/EOSDIS, NASA.  
> Available at: [https://earthdata.nasa.gov/earth-observation-data/near-real-time/citation](https://earthdata.nasa.gov/earth-observation-data/near-real-time/citation)

**Disclaimer**:  
The LANCE/FIRMS data is provided “as is” without warranty of any kind.  
Users assume all responsibility and liability for the use of this data, including any resulting loss, damage, or misuse.  
NASA and its data providers are not liable for any consequence of data use.

For full terms and guidance, refer to:  
- 🔗 [FIRMS FAQ](https://firms.modaps.eosdis.nasa.gov/faq/)  
- 🔗 [NASA Data Use Policy](https://earthdata.nasa.gov/earth-observation-data/data-use-policy)


## ⚠️ License

This project is intended for **academic use only** and is **not licensed for commercial or production deployment**.  
**No license is granted.**  
Please contact the authors for further usage rights.


## 🌐 Connect With Us

### 👨‍💻 Kanan Pandit  
🌐 [Portfolio](https://kananpanditportfolio.netlify.app/)  
✉️ kananpandit02@gmail.com  

### 👨‍💻 Sudam Paul  
🌐 [Portfolio](https://sudam23.github.io/My_Portfolio/)  
✉️ 2002sudam@gmail.com  

### 🏫 Institution  
**Ramakrishna Mission Vivekananda Educational and Research Institute**  
📍 *Belur Math, Howrah, West Bengal*
