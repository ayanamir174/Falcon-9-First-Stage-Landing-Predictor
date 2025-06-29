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

| Model                | Test Accuracy | F1 Score | Precision | Recall |
|---------------------|---------------|----------|-----------|--------|
| Logistic Regression | **83.3%**     | **89%**  | **92%**   | **87%** |
| SVM                 | **83.3%**     | 89%      | 91%       | 87%    |
| KNN                 | **83.3%**     | 84%      | 85%       | 83%    |
| Decision Tree       | 72.2%         | 72%      | 76%       | 69%    |

- All three models except the Decision Tree performed equally on test accuracy (**83.3%**), but **Logistic Regression** offered the best precision-recall balance.
- Trained on features such as `Payload Mass`, `Orbit`, `Launch Site`, and `Booster Version`.
- Dashboard supports filtering by **payload range**, **launch site**, and **outcome** for exploratory analysis.


---

## 📁 Files

| File | Description |
|------|-------------|
| `SpaceX_Landing_Predictor_Slides.pdf` | Slide deck summary |
| `SpaceX_Machine Learning Prediction_Part_5.ipynb`| Model training & evaluation                |
| `jupyter-labs-eda-sql-coursera_sqllite.ipynb`    | EDA & SQL-based transformations            |
| `jupyter-labs-spacex-data-collection-api.ipynb`  | API data collection and extraction logic   |
| `jupyter-labs-webscraping.ipynb`                 | Web scraping supplemental SpaceX data      |
| `lab_jupyter_launch_site_location.ipynb`         | Launch site data and location visualization|
| `labs-jupyter-spacex-Data wrangling.ipynb`       | Data cleaning and transformation           |
| `spacex_dash_app.py`                             | Dash app with visualizations               |
| `spacex_launch_dash.csv`                         | Cleaned dataset                            |
