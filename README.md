# Electric Vehicle Charging Demand Forecasting and Peak Load Risk Analysis

**Major Research Project (MRP)** | Master of Science in Data Science and Analytics  
Toronto Metropolitan University

---

## 📋 Project Overview

This research project presents a comprehensive data-driven framework to forecast short-term electric vehicle (EV) charging demand and identify peak load risk periods at public charging stations. The study compares six forecasting models spanning three families: ARIMA and SARIMA (statistical), XGBoost and Random Forest (machine learning), and LSTM and GRU (deep learning).

## 👤 Author

- **Name:** Karthik Raj Venkatesh
- **Student ID:** 501349198
- **Supervisor:** Dr. Saman Hassanzadeh Amin

## 🎯 Research Objectives

1. Perform exploratory data analysis (EDA) to identify temporal, operational, and geographic patterns in EV charging demand.
2. Develop forecasting models using ARIMA, SARIMA, Random Forest, XGBoost, LSTM, and GRU algorithms.
3. Compare statistical, machine learning, and deep learning approaches using RMSE and MAE metrics.
4. Identify peak-demand periods and charging station congestion risk.
5. Provide practical recommendations for charging station operators and infrastructure planners.

## 📊 Dataset

- **Source:** [Electric Vehicle Charging Station Availability Tracking Dataset (Kaggle)](https://www.kaggle.com/datasets/likithagedipudi/ev-charging-station-availability-tracking)
- **Size:** 100,000 records at 30-minute intervals
- **Duration:** July 1, 2025 to December 31, 2025 (6 months)
- **Coverage:** 12 charging stations across 7 cities
- **Cities:** Los Angeles, San Francisco, San Diego, Phoenix, Denver, Salt Lake City, Seattle
- **Features:** 33 columns including utilization metrics, temporal attributes, weather, traffic, and pricing variables

## 🔬 Models Compared

| Family | Models |
|--------|--------|
| **Statistical** | ARIMA(1,1,1), SARIMA(1,1,1)x(1,1,1,7) |
| **Machine Learning** | XGBoost, Random Forest |
| **Deep Learning** | LSTM (50 units), GRU (50 units) |

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `MRP_Milestone1_Comprehensive_EDA.ipynb` | Jupyter notebook with complete EDA code and visualizations |
| `ev_charging_station_data_100k.csv` | Dataset used for analysis |
| `Karthik_raj_EDA_report.pdf` | Milestone 1 report (Literature Review + EDA) |
| `README.md` | This file |

## 🔑 Key EDA Findings

- **Daily double-peak pattern:** noon (utilization 0.66) and 5-7 PM (0.52)
- **Weekday vs Weekend:** Weekdays show ~10% higher demand
- **Peak-load-risk window:** Weekday 11 AM - 7 PM
- **Geographic variation:** Los Angeles highest (0.58), Phoenix lowest (0.32)
- **Strongest predictors:** Hour of day (r = +0.455), Traffic congestion (r = +0.416)

## 🛠️ Tools & Technologies

- **Language:** Python 3.10
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, tensorflow/keras, statsmodels
- **Environment:** Google Colab + Jupyter Notebook
- **Version Control:** GitHub

## 📅 Project Milestones

| Milestone | Status | Due Date |
|-----------|--------|----------|
| Milestone 1: Literature Review + EDA | ✅ Complete | June 24, 2026 |
| Milestone 2: Methodology + Experiments | 🔄 In Progress | July 14, 2026 |
| Milestone 3: Results | ⏳ Upcoming | July 28, 2026 |
| Milestone 4: Final Project Report | ⏳ Upcoming | August 18, 2026 |
| Milestone 5: Poster Presentation | ⏳ Upcoming | August 20, 2026 |

## 📧 Contact

For questions about this project, please contact:
- **Author:** karthikraj.venkatesh@torontomu.ca
- **Supervisor:** saman.amin@torontomu.ca

## 📜 License

This project is for academic purposes as part of the Major Research Project requirement at Toronto Metropolitan University.
