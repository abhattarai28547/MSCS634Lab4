# MSCS634Lab4 - Regression Analysis with Regularization Techniques

**Name:** Avinna Bhattarai  
**Course:** MSCS 634 - Big Data and Data Mining  
**Lab Assignment:** Lab 4 - Multiple Regression and Regularization using the Diabetes Dataset

---

##  Purpose

This lab explores various regression techniques to model disease progression using the Diabetes dataset from `sklearn.datasets`. We implemented and compared:

- Simple Linear Regression
- Multiple Linear Regression
- Polynomial Regression (degrees 2–4)
- Ridge Regression
- Lasso Regression

The goal was to evaluate model performance, understand overfitting and underfitting, and apply regularization to improve generalization.

---

##  Methods & Models

- **Simple Linear Regression:** Used `bmi` feature to predict disease progression.
- **Multiple Linear Regression:** Used all 10 normalized features.
- **Polynomial Regression:** Tested polynomial degrees 2 through 4.
- **Ridge & Lasso:** Applied L2 and L1 regularization with scaled features.

Models were evaluated using:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

##  Key Findings

| Model                            | MAE   | RMSE  | R²     |
|----------------------------------|-------|--------|--------|
| Simple Linear Regression (BMI)  | 42.79 | 53.85  | 0.45   |
| Multiple Linear Regression       | 42.79 | 53.85  | 0.45   |
| Polynomial Regression (Deg=2)   | 43.58 | 55.64  | 0.42   |
| Polynomial Regression (Deg=3)   | 164.85| 287.13 | -14.56 |
| Polynomial Regression (Deg=4)   | 261.67| 383.29 | -26.73 |
| Ridge Regression (α=1.0)         | 42.81 | 53.78  | 0.45   |
| Lasso Regression (α=0.1)         | 42.80 | 53.71  | 0.46   |

###  Observations

- **`bmi`** is the strongest individual predictor.
- **Polynomial regression** (degrees 3 and 4) caused overfitting with poor generalization.
- **Ridge** slightly improved generalization over multiple linear regression.
- **Lasso** delivered the best overall performance (lowest RMSE, highest R²) and simplified the model by zeroing out less useful features.

---

##  Insights

- Regularization (Ridge/Lasso) is essential for controlling overfitting.
- Complex models aren’t always better — simpler, regularized models performed best.
- The Diabetes dataset’s relationships are mostly linear and additive.
- Lasso is particularly useful when we want a model that is both accurate and interpretable.

---

##  Challenges Faced

- Managing overfitting with polynomial models beyond degree 2.
- Visualizing and interpreting residuals helped diagnose poor model fit.
- Choosing meaningful `alpha` values for Ridge and Lasso.

---

##  Conclusion

This lab reinforced how model complexity and regularization affect regression performance. **Lasso Regression** stood out as the most practical model for this dataset — offering both accuracy and simplicity.

