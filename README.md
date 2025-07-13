
# ⚽ Football Player Market Value Prediction

This project uses machine learning regression models to **predict the market value of football players** based on various performance, demographic, and club-related features. It involves data preprocessing, exploratory data analysis, model evaluation, and hyperparameter tuning to achieve high prediction accuracy.

---

## 📌 Project Overview

Football clubs spend millions in the transfer market, and understanding what drives a player’s market value is crucial for clubs, agents, and fantasy football enthusiasts. This project aims to develop a predictive model using real-world football data to estimate a player's market value using:

- Age, Region, Position
- Fantasy Premier League (FPL) stats
- Player popularity (page views)
- Club information and transfer status

---

## 🔍 Dataset

- **Source**: Kaggle / public football stats
- **Filename**: `football player.csv`
- **Total Entries**: ~500 players
- **Features include**:
  - `age`, `position_cat`, `region`, `big_club`, `new_signing`
  - `fpl_value`, `fpl_points`, `fpl_sel`, `page_views`
  - `market_value` (target)

---

## 📊 Exploratory Data Analysis (EDA)

- Visualized distributions of age, FPL points, and market value
- Analyzed market value with respect to:
  - Region
  - Position category (Attack, Midfield, Defense, GK)
  - Big club membership
  - New signings
- Plotted a **correlation heatmap** of key numerical features

---

## ⚙️ Data Preprocessing

- Handled missing values and type conversions (e.g., `fpl_sel` from `%` string to float)
- One-hot encoded categorical features (`club`, `position`, `new_foreign`)
- Standardized features using **StandardScaler**
- Split dataset into **training (80%)** and **testing (20%)**

---

## 🤖 Machine Learning Models Used

A total of **8 regression models** were trained and evaluated:
- Linear Regression
- Lasso Regression
- Ridge Regression
- K-Nearest Neighbors (KNN)
- Support Vector Regression (SVR)
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

---

## 📈 Evaluation Metrics

Models were evaluated using:
- **R² Score** – Measure of model fit
- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**

A summary of all model results was printed and sorted based on R² scores.

---

## 🔧 Hyperparameter Tuning

Used **`RandomizedSearchCV`** and **`GridSearchCV`** to tune:
- **Random Forest Regressor**
- **Gradient Boosting Regressor**

Key hyperparameters optimized:
- `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`, `max_features`, `learning_rate`

---

## 🏁 Final Results

The **tuned ensemble models** (Random Forest and Gradient Boosting) gave the best results, significantly improving test performance.

Evaluation of the best-tuned models included final metrics on the test set.

---

## 📌 Future Work

- Integration with **SHAP/LIME** for model interpretability
- Deployment as a web app using **Streamlit**
- Experimentation with additional features (e.g., player nationality, contract duration)

---

## 🛠️ Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn
- Jupyter Notebook
- GridSearchCV / RandomizedSearchCV

---

## 📁 Project Structure

```
├── Football Player Market Value Prediction.ipynb  # Main notebook
├── football player.csv                            # Dataset
├── README.md
```

---

## ✍️ Author

**Pirishita Tuteja**  
3rd Year B.Tech CSE Student  
Machine Learning & Data Science Enthusiast

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
