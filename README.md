#  Predictive Maintenance & Cost Optimization Framework

##  Overview
This project proposes a robust **Predictive Maintenance (PdM) framework** for aircraft engines that bridges the gap between machine learning accuracy and real-world business economics. By integrating Remaining Useful Life (RUL) prediction models with a custom discrete-event cost simulator, this framework dynamically adjusts maintenance schedules based on **Prediction Uncertainty**, effectively minimizing both downtime risks and wasted asset life.

## Business Impact & Key Results
* **Cost Optimization:** Achieved an optimized average maintenance cost of **$8,420** per engine fleet, significantly outperforming traditional Point-Prediction PdM ($8,971) and Time-Based Maintenance strategies.
* **Risk Mitigation:** Designed an Uncertainty-Aware algorithm that incorporates moving standard deviations to penalize volatile predictions, virtually eliminating catastrophic downtime penalties.
* **Strategic Decision Making:** Conducted 2D Grid Search optimization (Threshold vs. Uncertainty Factor) to provide actionable insights for varying industrial cost structures.

##  Core Methodology
* **Data Processing:** Applied MinMax scaling and sliding window techniques (sequence length = 30) to transform NASA C-MAPSS FD001 multivariate time-series sensor data.
* **Predictive Modeling:** Evaluated Random Forest, XGBoost, and LSTM architectures. LSTM captured long-term degradation dependencies best (RMSE: 13.91), while XGBoost provided a strong balance of accuracy and interpretability.
* **Explainable AI (XAI):** Extracted global feature importance and visualized Decision Trees to validate that the model's logic aligns with physical domain knowledge (e.g., relying heavily on HPC outlet static pressure and LPT outlet temperature).

##  Tech Stack
* **Language:** Python
* **Machine Learning:** Scikit-learn, XGBoost
* **Deep Learning:** PyTorch (LSTM)
* **Data Analysis & Simulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn

##  Repository Structure
* `data/` : Instructions and links to download the NASA C-MAPSS dataset.
* `src/` : Source code for data preprocessing, model training (XGBoost, LSTM), and evaluation.
* `simulator/` : Custom Python-based time-series maintenance cost simulator.
* `docs/` : Detailed project report and presentation files.

## Main Author
* **Heejun Cho** * Connect with me on choheejun1114@gmail.com
