# 🌍 Environmental Air Quality & Ozone ($O_3$) Forecasting
**Collaborative Research with the Sharon-Carmel Municipal Environmental Association**

## 📖 Project Overview
This research analyzes the impact of the **"Leviathan" offshore gas platform** on air quality in the Sharon region, Israel. By integrating Big Data from multiple monitoring stations with advanced Machine Learning architectures, this project investigates whether the platform's activation led to a systematic increase in Ozone ($O_3$) concentrations.

## 🧭 Methodological Justification: Why Westerly Winds?
To isolate the platform's impact, the analysis focuses strictly on **Stable Westerly Winds** (25th-75th percentile speeds). Spatial sector analysis (Radar Plots) confirms that the highest Ozone concentrations arrive from the West (W) and North-West (NW) sectors—directly correlating with the offshore platform's location.

## 📊 Key Results & Statistical Audit
Our multi-stage analysis provides strong evidence of an operational impact on inland Ozone levels:

*   **Predictive Power:** The optimized **XGBoost** model achieved an **$R^2$ score of 0.361** on the test set, outperforming baseline linear models.
*   **Physical Contribution (Theta):** Linear Regression analysis revealed that the platform's operational status is a primary driver of Ozone increase, with a **Theta coefficient of 2.31** (the highest among predictors).
*   **Error Reduction:** Optimized models achieved an **RMSE to STD ratio of 0.81**, effectively reducing prediction uncertainty by approximately 19% compared to natural data variance.
*   **Significant Shifts:** Pairwise **Mann-Whitney U tests** confirmed statistically significant increases ($p < 0.05$) across all coastal stations, with a **12.6% rise** recorded at the "Hamapil" station.

## 🤖 Machine Learning & Innovation
### Predictive Models
To handle non-linear atmospheric interactions, we implemented and compared several architectures:
*   **Random Forest:** Optimized via `GridSearchCV` (max_depth=15, n_estimators=200).
*   **XGBoost:** The top-performing model for capturing complex meteorological patterns.
*   **Neural Network (MLP):** A 2-layer architecture (64 and 32 neurons) designed to model photochemical signatures.

### The LLM Edge
*   **Knowledge Extraction:** Leveraged Large Language Models (LLMs) to synthesize technical reports and scientific literature on Ozone precursors.
*   **Advanced Analytics:** Used AI-driven methodologies for data cleaning (Smart Imputation) and automated insight generation.

## 🛠️ Tech Stack
*   **Languages:** Python (Pandas, NumPy, SciPy)
*   **ML Frameworks:** Scikit-learn, XGBoost
*   **Visualization:** Matplotlib, Seaborn
*   **Environment:** Google Colab / Jupyter

---
*Note: This project follows a multi-stage pipeline involving KNN imputation for missing wind data and strict meteorological filtering. For academic or professional inquiries, please refer to the `Code.ipynb` file or contact me via GitHub.*
