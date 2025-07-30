# 🦄 Unicorn Valuation Analysis using Machine Learning & Clustering

This project analyzes the valuation of unicorn startups using machine learning models and clustering techniques. The goal was to understand what drives a startup’s valuation and to group similar startups based on investor-related metrics.

---

## 📁 Dataset

- **Source**: [Unicorn Companies Dataset](https://www.kaggle.com/datasets/startup-investments/unicorn-companies)
- **Shape**: 1186 rows × 7 columns
- **Fields** include:
  - Company Name
  - Industry
  - Valuation ($B)
  - Date Joined
  - Country
  - Investor Count
  - VC Power Score (custom metric)

---

## 🧪 Exploratory Data Analysis (EDA)

- Cleaned missing values and formatted date fields.
- Created a custom metric: **VC Power Score** to represent investor influence.
- Analyzed relationships between valuation, investor count, and funding year.

---

## 🤖 Predictive Modeling

### Models Trained:
1. Linear Regression  
2. Support Vector Regression (SVR)  
3. Decision Tree Regressor  
4. Random Forest Regressor  
5. XGBoost Regressor  

### 🔁 Techniques Used:
- Feature engineering (log valuation)
- Pipeline construction with scaling
- Grouping and handling categorical data

### 📊 Model Performance (After Scaling & Log Transformation):

| Model             | RMSE     | MAE      | R²       |
|------------------|----------|----------|----------|
| Random Forest     | 0.0040   | 0.0014   | 0.9999   |
| XGBoost           | 0.0067   | 0.0024   | 0.9998   |
| Decision Tree     | 0.0107   | 0.0025   | 0.9995   |
| SVR               | 0.1220   | 0.0829   | 0.9402   |
| Linear Regression | 0.2383   | 0.1867   | 0.7721   |

✅ Best Model: **Random Forest Regressor** (Highest R² and lowest error metrics)

---

## 📈 Clustering with K-Means

- Applied **PCA** to reduce dimensionality for better clustering.
- Used **Elbow Method** to determine optimal clusters → **k = 10**
- Grouped startups into 10 clusters based on:
  - Valuation
  - Investor Count
  - VC Power Score

### 🧾 Final Cluster Summary (Top 3 Examples):

| Cluster | Avg. Valuation ($B) | Investor Count | VC Power Score |
|---------|----------------------|----------------|----------------|
| 2       | 3.42                 | 2.91           | 1.0000         |
| 6       | 5.71                 | 2.78           | 0.0000         |
| 9       | 24.29                | 2.86           | 1.0600         |

---

## 📌 Insights & Conclusion

- Investor count alone does not explain valuation — **VC Power Score and timing matter significantly**.
- **Model performance improved drastically** after transformation and pipeline usage.
- Clustering highlighted groups of undervalued and overvalued startups.
- Potential applications: **investment prediction, startup scouting, VC strategy planning**.

---

## 📂 Files in This Repo

- `unicorn_valuation.ipynb`: Main notebook with code and visualizations.
- `README.md`: Project documentation.
- `cluster_summary.csv`: Cluster-wise metrics.
- `plots/`: Visualizations and SHAP explanations.

---

## 🚀 Future Improvements

- Incorporate text features like industry descriptions using NLP.
- Integrate funding round data for deeper analysis.
- Automate feature scoring using tools like SHAP or LIME.

---

## 🧠 Author

**Sam Caleb Blesson**  
Business Analyst Intern  
Contact: [LinkedIn](https://www.linkedin.com/in/your-profile) | [Kaggle](https://www.kaggle.com/samcalebblesson)

---

⭐ If you liked this project, feel free to fork it, star it, or use it as a reference for your own analysis!

