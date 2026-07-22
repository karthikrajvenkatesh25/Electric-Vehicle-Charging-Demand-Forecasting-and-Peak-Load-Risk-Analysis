Electric Vehicle Charging Demand Forecasting and Peak Load Risk Analysis

Major Research Project (MRP) | Master of Science in Data Science and Analytics Toronto Metropolitan University

📋 Project Overview

This research project presents a comprehensive data-driven framework to forecast short-term electric vehicle (EV) charging demand and identify peak load risk periods at public charging stations. The study compares six forecasting models spanning three families: ARIMA and SARIMA (statistical), XGBoost and Random Forest (machine learning), and LSTM and GRU (deep learning). Building on the exploratory analysis and model comparison from earlier milestones, the project also includes a dedicated peak-load-risk analysis that evaluates how each model performs specifically during high-demand periods.

👤 Author
Name: Karthik Raj Venkatesh
Student ID: 501349198
Supervisor: Dr. Saman Hassanzadeh Amin
🎯 Research Objectives
Perform exploratory data analysis (EDA) to identify temporal, operational, and geographic patterns in EV charging demand.
Develop forecasting models using ARIMA, SARIMA, Random Forest, XGBoost, LSTM, and GRU algorithms.
Compare statistical, machine learning, and deep learning approaches using RMSE and MAE metrics.
Identify peak-demand periods and charging station congestion risk.
Provide practical recommendations for charging station operators and infrastructure planners.
📊 Dataset
Source: Electric Vehicle Charging Station Availability Tracking Dataset (Kaggle)
Size: 100,000 records at 30-minute intervals
Duration: July 1, 2025 to December 31, 2025 (6 months)
Coverage: 12 charging stations across 7 cities
Cities: Los Angeles, Austin, San Diego, Minneapolis, Atlanta, Seattle, Phoenix
Features: 33 columns including utilization metrics, temporal attributes, weather, traffic, and pricing variables

⚠️ Note: city list corrected to match the Milestone 1 EDA report — please confirm this against your raw dataset before finalizing.

🔬 Models Compared
Family	Models
Statistical	ARIMA(1,1,1), SARIMA(1,1,1)x(1,1,1,7)
Machine Learning	XGBoost, Random Forest
Deep Learning	LSTM (50 units), GRU (50 units)
📁 Repository Contents
File	Description
MRP_Milestone1_Comprehensive_EDA.ipynb	Jupyter notebook with EDA, all six forecasting models, and the peak-load-risk analysis
ev_charging_station_data_100k.csv	Dataset used for analysis
Karthik_raj_EDA_report.pdf	Milestone 1 report (Literature Review + EDA)
Karthik_Raj_MRP_Methodology_and_Experiments.pdf	Milestone 2 report (Methodology + Experiments)
Karthik_Raj_MRP_Milestone3_Results.docx	Milestone 3 report (Results and Discussion + Peak-Load-Risk Analysis)
README.md	This file
🔑 Key EDA Findings
Daily double-peak pattern: noon (utilization 0.66) and 5-7 PM (0.52)
Weekday vs Weekend: Weekdays show ~10% higher demand
Peak-load-risk window: Weekday 11 AM - 7 PM, especially Tuesday-Thursday
Geographic variation: Los Angeles highest (0.58), Phoenix lowest (0.32)
Strongest predictors: Hour of day (r = +0.455), Traffic congestion (r = +0.416)
📈 Model Comparison Results
Model	Family	RMSE	MAE
Random Forest	Machine Learning	0.0451	0.0112
XGBoost	Machine Learning	0.0451	0.0097
ARIMA(1,1,1)	Statistical	0.0468	0.0249
LSTM (50 units)	Deep Learning	0.0471	0.0291
GRU (50 units)	Deep Learning	0.0474	0.0245
SARIMA(1,1,1)x(1,1,1,7)	Statistical	0.0493	0.0178

XGBoost achieved the best overall performance (lowest MAE) and remained the most accurate model during both peak-risk and non-peak periods.

Note: LSTM and GRU do not use a fixed random seed, so their exact values shift slightly between full notebook re-runs. The numbers above reflect the most recent run.

🚦 Peak-Load-Risk Analysis

Peak-risk days were defined as days above the 90th percentile of daily utilization, computed from training/validation data only. In the 37-day test period, 23 days (62.2%) were flagged as peak-risk, concentrated on Tuesday and Thursday — consistent with the hourly peak-risk heatmap from the EDA phase.

Every model showed lower error on peak-risk days than on non-peak days. This is because the peak-risk period formed a stable, elevated plateau that was relatively easy to predict once a model adjusted to it, while the non-peak period contained a sharp, unexpected drop in utilization that increased error across all six models — a reminder that overall accuracy alone does not capture how a model handles sudden, unexpected shifts in demand.

🛠️ Tools & Technologies
Language: Python 3.10
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, tensorflow/keras, statsmodels
Environment: Google Colab + Jupyter Notebook
Version Control: GitHub
📅 Project Milestones
Milestone	Status	Due Date
Milestone 1: Literature Review + EDA	✅ Complete	June 24, 2026
Milestone 2: Methodology + Experiments	✅ Complete	July 14, 2026
Milestone 3: Results	✅ Complete	July 28, 2026
Milestone 4: Final Project Report	⏳ Upcoming	August 18, 2026
Milestone 5: Poster Presentation	⏳ Upcoming	August 20, 2026
📚 References
Abdel-Aziz, M. (2026). Electric vehicles charging stations load forecasting based on hybrid XGBoost-BiLSTM model. Scientific Reports, 16(1), 374.
Box, G. E. P., Jenkins, G. M., Reinsel, G. C., & Ljung, G. M. (2015). Time series analysis: Forecasting and control (5th ed.). Wiley.
Chen, T., & Guestrin, C. (2016). XGBoost: A scalable tree boosting system. Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, 785–794.
Gedipudi, L. (2023). Electric vehicle charging station availability tracking dataset. Kaggle.
Hochreiter, S., & Schmidhuber, J. (1997). Long short-term memory. Neural Computation, 9(8), 1735–1780.
Shanmuganathan, J., Victoire, A. A., Balraj, G., & Victoire, A. (2022). Deep learning LSTM recurrent neural network model for prediction of electric vehicle charging demand. Sustainability, 14(16), 10207.
Yi, Z., Liu, X. C., Wei, R., Chen, X., & Dai, J. (2022). Electric vehicle charging demand forecasting using deep learning model. Journal of Intelligent Transportation Systems, 26(6), 690–703.
📧 Contact

For questions about this project, please contact:

Author: karthikraj.venkatesh@torontomu.ca
Supervisor: saman.amin@torontomu.ca
📜 License

This project is for academic purposes as part of the Major Research Project requirement at Toronto Metropolitan University.
