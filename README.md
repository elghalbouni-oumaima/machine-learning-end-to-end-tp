# machine-learning-end-to-end-tp
End-to-end machine learning project using regression and classification on Kaggle datasets.


# 🤖 Multi-Domain Machine Learning: Housing & Fashion

This repository contains two distinct machine learning projects showcasing  data preprocessing, feature engineering, and model optimization using "traditional" (non-neural) machine learning algorithms.

---

## 🏠 Project 1: Ames Housing Price Prediction (Regression)

**Goal:** Predict the final price of residential homes in Ames, Iowa, based on 79 explanatory variables.

### 🛠️ Feature Engineering & Logic

A key highlight of this project is the custom feature engineering aimed at reducing dimensionality and increasing model stability.

* **Total Square Footage:** Combined `GrLivArea` and `TotalBsmtSF` to create a single "Power Feature."
* **Advanced Bathroom Calculation:** Created a weighted `total_baths` feature:



*Note: Half-baths are weighted at 0.5 to reflect their actual real estate value.*

### 📈 Model Performance

| Model | RMSE (Mean) | Std Deviation |
| --- | --- | --- |
| **ElasticNet** | 0.1102 | 0.0081 |
| **XGBoost** | 0.1120 | 0.0074 |

*The XGBoost model showed superior stability (lower Std Dev), suggesting better generalization on unseen data.*

---

## 👕 Project 2: Fashion-MNIST Image Classification

**Goal:** Classify 60,000 grayscale images (28x28) of clothing into 10 categories.



### 🧠 Models Evaluated

1. **Logistic Regression:** Used the `multinomial` strategy with the `SAGA` solver for high-speed convergence on 60,000 rows.
2. **SVC (Support Vector Classification):** Utilized the "Kernel Trick" (RBF) to find optimal hyperplanes between clothing categories.
3. **XGBoost Classifier:** Applied to image pixels to capture non-linear relationships without a CNN.

---

## 🚀 Key Technologies

* **Python 3.x**
* **Scikit-Learn:** LogisticRegression, SVC, ElasticNet, PCA.
* **XGBoost:** Gradient Boosted Decision Trees.
* **TensorFlow/Keras:** Used specifically for the `ImageDataGenerator` augmentation logic.
* **Pandas/NumPy:** Data manipulation and matrix math.

---

## 📂 Project Structure

```text
├── Ames_Housing_Analysis.ipynb    # Housing Regression Notebook
├── Fashion_MNIST_Classif.ipynb    # Image Classification Notebook
└── README.md

```

---

## 💡 Summary of Skills

* **Domain Adaptation:** Successfully applied ML to both financial (Housing) and visual (Fashion) data.
* **Mathematical Insight:** Implemented weighted features and multinomial classification strategies.
* **Efficiency:** Optimized traditional models to handle large datasets (60k rows) effectively.

