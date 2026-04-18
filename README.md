# 🌍 Environmental Air Quality & Ozone ($O_3$) Forecasting
**Collaborative Research with the Sharon-Carmel Municipal Environmental Association**

## 📖 Project Overview
This research investigates the environmental impact of the **"Leviathan" offshore gas platform** on coastal air quality in Israel. By integrating multi-station meteorological data with advanced Machine Learning architectures, the project quantifies how the platform's activation influenced ground-level Ozone ($O_3$) concentrations. 

This project demonstrates a full data science pipeline: from complex data engineering and "smart" imputation to non-linear modeling and physical interpretation.

## 🧭 Methodological Justification: Stable Westerly Winds
A core challenge in environmental modeling is isolating a specific source from background noise. This study focuses on **Stable Westerly Winds** (filtering for 25th-75th percentile speeds) to isolate air masses arriving directly from the offshore platform toward inland monitoring stations.

<p align="center">
  <img src="wind_sector_analysis.png" width="500" alt="Spatial Sector Analysis">
  <br><i>Figure 1: Spatial sector analysis confirming $O_3$ transport from the Western/North-Western maritime sectors.</i>
</p>

## 📊 Key Results & Statistical Significance
The analysis provides robust evidence of an operational impact on inland Ozone levels:

*   **Predictive Power:** The optimized **XGBoost** model achieved an **$R^2$ score of 0.361** on the test set, significantly outperforming baseline linear regression.
*   **Physical Contribution (Theta):** Linear coefficients identify the platform's operational status as a dominant predictor, with a **Theta coefficient of 2.31**—the highest among all features.
*   **Error Reduction:** Optimized models reached an **RMSE to STD ratio of 0.81**, reducing prediction uncertainty by **19%** compared to natural data variance.
*   **Statistical Audit:** Pairwise **Mann-Whitney U tests** confirmed statistically significant shifts ($p < 0.05$) in $O_3$ distributions, including a **12.6% rise** at the "Hamapil" coastal station.

<p align="center">
  <img src="model_performance_comparison.png" width="700" alt="Model Comparison">
  <br><i>Figure 2: Comparative performance of Linear, Tree-based, and Neural Network architectures.</i>
</p>

## 🤖 Machine Learning & Innovation
### Feature Importance
Beyond simple correlation, the models identified the synergistic effects of solar radiation, temperature, and operational status in driving photochemical $O_3$ production.

<p align="center">
  <img src="final_feature_importance.png" width="600" alt="Feature Importance">
  <br><i>Figure 3: Relative feature importance rankings highlighting the impact of operational status.</i>
</p>

### Technical Excellence
*   **Advanced Imputation:** Implemented a hybrid pipeline using **KNN Imputation** for wind vectors and **Linear Regression** for meteorological gaps to ensure dataset integrity.
*   **Architectures:** Comparison of Random Forest (GridSearchCV optimized), XGBoost, and a **Multi-Layer Perceptron (Neural Network)** with a 64/32 hidden layer configuration.
*   **LLM Integration:** Utilized Large Language Models for automated scientific insight extraction and literature synthesis.

## 📂 Repository Structure
*   `Code.ipynb`: Complete research notebook (EDA, Preprocessing, Modeling, and Evaluation).
*   `Final_Research_Model_Metrics.xlsx`: Detailed audit log of all model iterations and statistical metrics.
*   `outputs/`: High-resolution visualizations and performance plots.

## 🛠️ Tech Stack
*   **Languages:** Python (Pandas, NumPy, SciPy)
*   **ML Frameworks:** Scikit-learn, XGBoost
*   **Visualization:** Matplotlib, Seaborn

---
## 📄 Note on Data Confidentiality
*Due to confidentiality agreements with the Sharon-Carmel Municipal Environmental Association, the raw datasets are not included in this repository. The project highlights the methodological framework and analytical outcomes using real-world sensitive data. For inquiries regarding the methodology, please contact me.*
