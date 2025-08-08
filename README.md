# Salary Prediction – Comparing Linear Regression Models
##  Overview
This project predicts **salary** based on **years of experience** using different regression models.  The aim is to compare how various linear and non-linear approaches perform on the same dataset.
## 📊 Dataset
- **Source:** Kaggle – Salary Dataset for Simple Linear Regression   
- **Features:**
  - `YearsExperience` – Number of years of professional experience  
  - `Salary` – Annual salary in USD  


## ⚙️ Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-Learn
- SciPy


## 🚀 Models Tested
1. **Linear Regression**  
2. **Ridge Regression**  
3. **Polynomial Regression** (degree 2, 3, 4)  
4. **Univariate Spline Regression** (2, 3, and 5 segments)


## 📊 Visualizations
- Scatter plot of **Years of Experience vs Salary**
- Regression lines for each model
- Comparison chart of R² scores

## 📖 Understanding Linear Regression

**Linear Regression** is a method to predict a value (Salary) from another value (Years of Experience) by fitting a straight line to the data.

The equation of the line is:

$$
\hat{Y} = \beta_0 + \beta_1 X
$$

Where:
- \( \hat{Y} \) = predicted salary  
- \( X \) = years of experience  
- \( \beta_0 \) = starting salary (intercept)  
- \( \beta_1 \) = increase in salary per extra year (slope)  

---

### 📝 Steps
1. **Collect the data** → Years of Experience and Salary  
2. **Fit the line** → Find \(\beta_0\) and \(\beta_1\) that best match the data  
3. **Predict** → Use the line to estimate salary for new experience values  
4. **Evaluate** → Check how well the line fits using \(R^2\) score  

---

### 📊 What is \(R^2\)?
The \(R^2\) score tells us how much of the salary variation is explained by our model.

Formula:

$$
R^2 = 1 - \frac{\text{Sum of Squared Errors}}{\text{Total Variation}}
$$

- \(R^2 = 1\) → Perfect fit  
- \(R^2 = 0\) → Model is no better than guessing the average salary  
- \(R^2 < 0\) → Model is worse than just using the average salary  

---
## 📖 Understanding Spline Regression

**Spline Regression** fits a curve to data by breaking the X-axis into smaller sections (**segments**) and fitting a separate polynomial in each section.  
The sections are connected at special points called **knots**, and the curve is kept smooth at these knots so there are no sharp corners.

---

### 🔹 Why use Splines?
- A single straight line (Linear Regression) might be too simple.  
- One big polynomial can be too wiggly or unstable.  
- Splines give a **good balance**: flexibility in different regions without overfitting everywhere.

---
## 📈 Model Comparison Results

| Regression Type     | R² Score  |
|---------------------|----------:|
| Spline – 5 Segments | **0.9781** |
| Spline – 3 Segments | 0.9669    |
| Spline – 2 Segments | 0.9637    |
| Polynomial – Degree 2 | 0.9048 |
| Polynomial – Degree 4 | 0.9030 |
| Linear Regression   | 0.9024    |
| Ridge Regression    | 0.9022    |
| Polynomial – Degree 2 (alt) | 0.8972 |


