# Linear Regression Numerical Methods

Comparative analysis of numerical methods for linear regression applied to the WHO global life expectancy dataset.

## Project Description

This repository contains the implementation and analysis of five different numerical methods for solving linear regression problems. The research compares direct methods (Least Squares, SVD, QR Decomposition) and iterative methods (Conjugate Gradient, Adam Optimization), evaluating their computational efficiency, numerical stability, and predictive performance.

The dataset used is the "Life Expectancy Data" from the World Health Organization (WHO), which contains health, socioeconomic, and demographic indicators for different countries during the period 2000-2015.

## Repository Contents
```bash
linear-regression-numerical-methods
├── Life Expectancy Data.csv.xls  # WHO dataset on life expectancy
├── linear-regression-tutorial.ipynb  # Jupyter notebook with method implementations and analysis
├── notebook.pdf  # PDF version of Jupyter notebook
├── NumericalAnalysis_Report.pdf  # Official documentation
└── README.md   # This file
```

## Implemented Methods

### Direct Methods
1. **Least Squares (Normal Equations)** - Direct solution of $(X^TX)^{-1}X^Ty$
2. **Singular Value Decomposition (SVD)** - Using the decomposition $X = U\Sigma V^T$
3. **QR Decomposition** - Using the decomposition $X = QR$

### Iterative Methods
4. **Conjugate Gradient** - Iterative algorithm optimized for quadratic functions
5. **Adam Optimization** - Adaptive gradient optimization algorithm

## Main Results

- Direct methods and Conjugate Gradient converge to the same solution for well-conditioned problems
- Conjugate Gradient shows drastically faster convergence compared to Adam (≈10 vs >500 iterations)
- Extending to a polynomial model of degree 2 reduces the error by 40% compared to the linear model, highlighting the non-linear nature of relationships in the dataset

## How to Use

#### Clone the repository

```bash
git clone https://github.com/yourusername/linear-regression-numerical-methods.git
cd linear-regression-numerical-methods
```

#### Install dependencies
```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

#### Start Jupyter Notebook
```bash
jupyter notebook linear-regression-tutorial.ipynb
```

## Notebook Structure

The `linear-regression-tutorial.ipynb` notebook is organized into the following sections:

1. Definition & Working principle: Introduces linear regression, its principles, and the hypothesis representation for simple and multiple regression.
2. Import Library and Dataset: Importing necessary Python libraries and loading the dataset.
3. 📊 Dataset Structure: Description of the dataset structure, feature details, analysis objective, and an example regression equation.
4. Matrix Formulation: Explanation of the matrix formulation for linear regression.
5. Cost function: Definition of the cost function (OLS/MSE) and its matrix representation.
6. Normal Equation: Mathematical derivation of the Normal Equation to analytically solve linear regression.
7. Problem of Ill-Conditioning and Multicollinearity in Regression Models: Discussion of the multicollinearity problem, its effects, and solutions (Ridge and Lasso Regression).
8. Exploratory data analysis: Exploratory data analysis, including graphs such as:
  - Relationship between GDP and Life Expectancy (lmplot)
  - Correlation Matrix
  - Violin Plot Analysis (Life Expectancy vs Status; GDP vs Status)
  - Boxplot Analysis (Life Expectancy vs GDP Category and Status)
  - Scatter Plot (Life Expectancy vs GDP, with HIV/AIDS as hue)
9. Data Preprocessing: Data preprocessing steps, including splitting into training and test sets and normalization.
10. Model Building: Definition and implementation of different regression models (Least Squares, SVD, QR, Conjugate Gradient, Adam). Includes evaluation of these models.
11. Polynomial Model with Ridge Regularization: Explanation and implementation of polynomial regression with Ridge regularization.
12. Linear vs. Polynomial Model: Performance comparison between the simple linear model and the regularized polynomial model.
13. 📌 Conclusions: Summary of results, key learnings, and final considerations.

## Requirements

- Python 3.6+
- NumPy
- Pandas
- Matplotlib
- Scikit-learn 
- Jupyter Notebook

## Author

Alfio Spoto - University of Catania  
Department of Mathematics and Computer Science

## References

- Golub, G. H., & Van Loan, C. F. (2013). Matrix Computations (4th ed.)
- Nocedal, J., & Wright, S. J. (2006). Numerical Optimization (2nd ed.)
- Kingma, D. P., & Ba, J. (2014). Adam: A Method for Stochastic Optimization
- Hestenes, M. R., & Stiefel, E. (1952). Methods of Conjugate Gradients for Solving Linear Systems
- Dataset: WHO Life Expectancy Data (2000-2015)