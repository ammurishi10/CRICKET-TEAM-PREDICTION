# 🏏 Cricket Team Selection – Balanced Playing XI using Machine Learning

This project aims to automate and optimize the selection of a **balanced playing XI** in cricket using player performance data and machine learning. By analyzing historical stats in batting, bowling, and fielding, the system predicts whether a player deserves selection. This approach minimizes subjectivity and introduces a **data-driven framework** for team building across formats, making it applicable to fantasy cricket, domestic league analysis, and national selection support.

---

## 📂 Dataset Source
Kaggle:https://www.kaggle.com/datasets/mahendran1/icc-cricket

---

## 🧰 Tools & Technologies Used

- **Programming Language:** Python  
- **Data Handling:** Pandas, NumPy  
- **Data Visualization:** Matplotlib, Seaborn  
- **Machine Learning Models:** Scikit-learn  
- **Development Environment:** Jupyter Notebook  

---

## 🔍 Machine Learning Pipeline

1. **Data Preprocessing**
   - Merged batting, bowling, and fielding datasets on player name
   - Handled missing values and filtered relevant columns
   - Normalized metrics to balance scale across skills

2. **Feature Engineering**
   - Computed a **custom performance score** per player using weighted contributions:
     - Batters: based on `Runs`, `Avg`, `SR`
     - Bowlers: based on `Wickets`, `Econ`, `Avg`
     - Fielders/Wicketkeepers: based on `Dismissals`, `Ct`, `St`
   - Labeled players as `Selected = Yes/No` based on thresholds for each role

3. **Model Building**
Several classification algorithms were tested to predict player selection based on performance data. Each model was evaluated for accuracy, interpretability, and suitability for the task.

• **Logistic Regression**  
A linear model used as a baseline. It's simple, fast, and easy to interpret, but limited to linear relationships and underperformed on non-linear patterns.

• **Decision Tree Classifier** ✅  
This model creates rule-based branches for decision-making. It was chosen as the final model due to its interpretability, good performance, and ability to handle complex, non-linear data without much tuning. It clearly explained the reasoning behind player inclusion or exclusion.

• **Random Forest Classifier**  
An ensemble of decision trees that generally improves accuracy and reduces overfitting. While effective, it is less interpretable than a single decision tree and slower to compute.

• **K-Nearest Neighbors (KNN)**  
A non-parametric model that classifies based on distance to neighboring data points. It performed decently but was sensitive to scaling and less effective in high-dimensional spaces.

• **Support Vector Classifier (SVC)**  
This model attempts to find the optimal margin between classes. It handled the classification well but was computationally heavier and harder to interpret in the context of explaining player selections.

✅ **Final Selection:**  
The **Decision Tree Classifier** was selected for this project due to its balance of accuracy, speed, and clear, explainable output. It allowed transparent justification for each player's selection, aligning well with the project’s goal of data-driven but understandable team building.

    

4. **Evaluation**
   - Metrics: **Accuracy**, **Confusion Matrix**, **Precision**, **Recall**, **F1-Score**
   - Model explained through visualizations and prediction probabilities

---

##  Results & Insights

- The final model accurately predicted team inclusion with high confidence.
- Top batters had high `Avg` and `SR`, while top bowlers balanced `Wickets` with `Economy`.
- All-rounders and wicketkeepers were identified using combined batting, bowling, and fielding contributions.
- A **balanced playing XI** was selected with:
  -  5 Batters  
  -  3 Bowlers  
  -  2 All-Rounders  
  -  1 Wicketkeeper  
- The system ensures role diversity while maximizing performance potential based on real stats.
- Can be scaled for **fantasy leagues**, **domestic selection**, or **match-specific conditions**.

---


## 👤 Author

**K Rishika**  
Data Science | Machine Learning | Data Analytics


