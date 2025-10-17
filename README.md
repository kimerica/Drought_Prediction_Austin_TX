# Drought Analysis & Prediction (Time-Series) - Camp Mabry, Austin TX (1940-2020)

This project analyzes long-term climate records from Austin’s Camp Mabry to explore drought patterns and build baseline forecasts using simple, explainable time-series models.

---

## Dataset

- **Source:** Data USA:(https://datausa.io/api/data?drilldowns=Nation&measures=Population)
- **Format:** Daily observations resampled to monthly for modeling
- **Size:** ~81 years (≈ 972 monthly records)
- **Features:** precipitation, temperature min/mean/max, and related weather variables
- **Target (label):** Drought — created using precipitation & temperature quantile thresholds (binary: 1 = drought, 0 = not drought)
  
---

## Tools & Libraries

- **Python Libraries:** `pandas`, `scikit-learn`, `numpy`, `seaborn`, `matplotlib`, `statsmodels`, `jupyter`
- **Techniques:** data cleaning, feature selection, train/test split, classification evaluation
- **Models Compared:**
  - Logistic Regression
  - XGBoost Classifier
  - K-Means (unsupervised exploration / sanity check)
    
---

## Workflow

1. Load and clean Camp Mabry climate data (handle missing values and outliers as needed).
2. Build the Drought label from precipitation & temperature quantile rules.
3. Select features and create the train/test split.
4. Train classifiers (Logistic Regression, XGBoost).
5. Evaluate with:
   - Accuracy, Precision, Recall, F1 (classification_report)
   - Confusion Matrix (per-class performance)
6. Explore K-Means clusters and compare to the Drought label.
7. Summarize trade-offs (e.g., precision vs. recall) and pick a default model.
---

## Results

- Confusion matrices and full classification reports are printed for each model in the notebook.
- K-Means gives an unsupervised view of natural groupings and their alignment with the drought label.
- See the final section of the notebook for metrics and discussion.
---

## How to Run

1. Clone this repository
2. Install required libraries (`pandas`, `scikit-learn`, `numpy`, `seaborn`, `matplotlib`, `statsmodels`, `jupyter`).
3. Open the notebook `Climate_Modeling_Final.ipynb` and run cells in order.


---

## Author

**Erica Kim**  
Master’s in Data Science – University of Colorado Boulder  
[GitHub Profile](https://github.com/kimerica)
