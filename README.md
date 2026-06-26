# Customer Segmentation & Predictive Analytics Project

##  Project Overview
This project focuses on analyzing customer behavior and data from a marketing campaign dataset. By leveraging **Machine Learning (Supervised and Unsupervised Learning)**, the project delivers data-driven insights to optimize marketing strategies, predict customer spending, evaluate campaign responses, and segment the customer base effectively.

---

##  Key Features & Methodology

### 1. Data Preprocessing & Feature Engineering
* **Missing Value Imputation:** Handled missing values in the `Income` column using the Median strategy.
* **Feature Engineering:** Developed 3 critical domain-specific features:
  * `Age`: Calculated based on the birth year (relative to the current academic year 2026).
  * `TotalSpending`: Summed across all product categories (Wines, Fruits, Meat, Fish, Sweets, Gold).
  * `TotalChildren`: Combined `Kidhome` and `Teenhome` to understand household dynamics.
* **Data Cleansing:** Filtered out unrealistic ages (outside 18–100) and removed zero-income anomalies.
* **Categorical Encoding:** Applied Ordinal Label Encoding for `Education` and One-Hot Encoding for `Marital_Status`.

### 2. Supervised Learning: Regression
* **Target Variable:** `TotalSpending`
* **Models Trained:** Linear Regression, Ridge Regression ($\alpha=1.0$), and Decision Tree Regressor.
* **Evaluation Metrics:** Evaluated using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and $R^2$ Score.
* **Insights:** Ridge Regression was utilized to mitigate potential multicollinearity among correlated numerical features.

### 3. Supervised Learning: Classification
* **Target Variable:** `Response` (Binary classification for last campaign acceptance).
* **Class Imbalance:** Inspected and handled the baseline class imbalance in customer responses.
* **Models Trained:** Logistic Regression (with balanced class weights), K-Nearest Neighbors (KNN), and Random Forest Classifier.
* **Evaluation:** Evaluated via Confusion Matrices and Classification Reports (Precision, Recall, F1-Score).

### 4. Unsupervised Learning: Clustering (Customer Segmentation)
* **Features Used:** `TotalSpending`, `Income`, `Age`, `TotalChildren`.
* **Optimal Clusters ($k$):** Determined using the **Elbow Method** (Inertia vs. Number of Clusters).
* **Dimensionality Reduction:** Applied **Principal Component Analysis (PCA)** to project the 4-dimensional data into 2D for interactive scatter plot visualization.
* **Cluster Profiling:** Computed the mean values of each group to identify distinct customer personas.

---

##  Tech Stack & Libraries
* **Language:** Python
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `kagglehub`

---

##  How to Run the Project
1. Clone this repository or open the `.ipynb` file in **Google Colab**.
2. Run the first cell.
3. When prompted, enter your **Kaggle Username** and **Kaggle API Key** interactively to securely download the dataset via `kagglehub`.
4. Execute the remaining cells sequentially to view the training metrics, logs, and visualizations.
