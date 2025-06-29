# 🚀 Falcon 9 First Stage Landing Predictor

This project uses machine learning to predict whether the **first stage of a Falcon 9 rocket** will successfully land after launch. 

SpaceX advertises Falcon 9 launches at **$62 million**, significantly cheaper than other providers charging **$165+ million**. Much of the cost advantage comes from **reusing the first stage**. Accurately predicting successful landings can help external companies **evaluate SpaceX’s pricing model** or make informed bids against SpaceX for commercial launches.

---

## 📄 Project Summary

👉 [**View Slide Deck (PDF)**](./Project%20Summary.pdf)

---

## ❓ Problem Statement

> Can we predict whether the Falcon 9 first stage will land successfully based on pre-launch attributes such as payload mass, orbit, and launch site?

---

## 🛠 Tools Used

- **Languages:** Python  
- **Libraries:** Pandas, Scikit-learn, Plotly, Dash, BeautifulSoup  
- **Data Sources:** SpaceX Launch API, SpaceX website (scraped), public launch records

---

## 🔁 Workflow

1. **Data Collection**
   - Retrieved launch data using a combination of **API calls** and **web scraping**
   - Compiled structured dataset containing payload mass, orbit type, launch site, booster version, and landing outcome

2. **Data Wrangling**
   - Cleaned and encoded features (categorical encoding, missing value imputation, data type casting)
   - Engineered features like orbit, booster version, and launch pad

3. **Modeling**
   - Trained classification models:  
     - Logistic Regression  
     - Support Vector Machine (SVM)  
     - K-Nearest Neighbors (KNN)  
     - Decision Tree  
   - Evaluated using test accuracy and visualization

4. **Visualization**
   - Created an **interactive dashboard using Dash and Plotly** to visualize:
     - Landing outcomes by launch site
     - Correlation between payload and success
     - Success/failure distribution across filters

---

## 📈 Key Results

| Model                | Test Accuracy |
|---------------------|---------------|
| Logistic Regression | **83.3%**     |
| SVM                 | **83.3%**     |
| KNN                 | **83.3%**     |
| Decision Tree       | **72.2%**     |

- Landing success is **positively correlated with lower payload mass** and **certain booster versions**
- Dashboard enables filtering by launch site and payload range

---

## 📊 Dashboard Preview

<img src="screenshots/dashboard_all_sites.png" alt="Dashboard Example" width="600"/>
*(Interactive dashboard included in this repo)*

---

## 📁 Files

| File | Description |
|------|-------------|
| `spacex_dash_app.py` | Dash app with visualizations |
| `spacex_launch_dash.csv` | Cleaned dataset |
| `SpaceX_Machine Learning Prediction_Part_5.ipynb` | Model training & evaluation |
| `jupyter-labs-eda-sql-coursera_sqllite.ipynb` | EDA & SQL-based transformations |
| `labs-jupyter-spacex-Data wrangling.ipynb` | Feature engineering |
| `SpaceX_Landing_Predictor_Slides.pdf` | Slide deck summary |
