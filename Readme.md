## Movie Rating Prediction Project

**Student:** Neta Or Shaul  

---

### Project Overview

This project builds a machine learning model to predict movie ratings (averageRating) based only on information available before the movie release.

The solution focuses on feature engineering using historical data, genre information, and director-based features in order to capture patterns in the dataset.

The main preprocessing step is handled by the prepare_data function, which creates the final feature set.

After comparing multiple models, Random Forest was selected as the final model.

---

### How to Run

- Install requirements:
  pip install -r requirements.txt  

- Open the notebook  

- Run all cells in order:
  - Load the data  
  - Split into train and test  
  - Generate features using the prepare_data function  
  - Train models and evaluate results  

---

### Data Processing & Methodology

- **Feature Engineering:**  
  Created advanced features based on historical statistics, genres, and directors  

- **Data leakage prevention:**  
  All historical features were calculated using past data only  

- **Models:**  
  Compared ElasticNet and Random Forest using Cross Validation  

- **Evaluation:**  
  Used RMSE, MAE, and R² to compare model performance and stability  

---

### Key Insights

- The model performs well on general patterns but struggles with extreme values (outliers)  
- Historical features such as genre and director have the strongest influence on predictions  
- The model tends to predict values close to the average  

---

### File Structure

- notebook.ipynb – Full pipeline (feature engineering, training, evaluation)  
- model.pkl – Final model (Random Forest – best performing model)  
- elastic_model.pkl – ElasticNet model (reference model)  
- mappings.pkl – Precomputed statistical mappings for feature engineering  
- report.pdf – Final project report with analysis and results  
- requirements.txt – Required Python libraries  
- README.md – Project documentation  

---

### Notes

- Data leakage was carefully prevented during feature creation  
- Precomputed mappings are saved and loaded from a file and are used in the prepare_data function so it can run independently and use previously computed values instead of recalculating them each time  