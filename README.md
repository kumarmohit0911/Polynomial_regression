# Polynomial Regression for Quadratic Dataset

## Overview
This project demonstrates the application of **Polynomial Regression** to a synthetic quadratic dataset. The dataset is generated using a quadratic equation with some added noise, and the model aims to improve prediction accuracy compared to simple linear regression.

The project compares the performance of **Simple Linear Regression** and **Polynomial Regression**, highlighting the advantage of using polynomial features for non-linear datasets.

## Features
- Generate synthetic data based on a quadratic equation.
- Visualize the dataset and regression models.
- Apply **Simple Linear Regression** and evaluate its performance.
- Use **Polynomial Regression** with adjustable degrees to improve accuracy.
- Predict outcomes for new data points.

## Dataset
The dataset is generated programmatically:
- \( y = 0.5x^2 + 1.5x + 2 + \text{noise} \)
- \( x \) values are uniformly distributed between -3 and 3.
- Noise is added using a normal distribution for realistic variation.

## Libraries Used
- **pandas**: For data manipulation.
- **numpy**: For numerical computations and dataset generation.
- **matplotlib**: For data visualization.
- **scikit-learn**: For regression models and performance metrics.

## Steps

### 1. Generate Synthetic Data
The data is created using the quadratic equation \( y = 0.5x^2 + 1.5x + 2 + \text{noise} \), with \( x \) values randomly sampled between -3 and 3. The generated data is visualized using a scatter plot.

### 2. Train-Test Split
The data is split into training and testing sets using an 80-20 ratio with `train_test_split` from scikit-learn.

### 3. Simple Linear Regression
A simple linear regression model is trained on the dataset. However, due to the non-linear nature of the data, the model performs poorly, resulting in a low \( R^2 \) score. 

The limitations of linear regression for non-linear datasets are visualized using a best-fit line plot.

### 4. Polynomial Regression
To address the non-linearity, polynomial features are generated using `PolynomialFeatures` from scikit-learn. Two different degrees of polynomial features are tested:
- **Degree = 2**: Captures the quadratic relationship in the data.
- **Degree = 3**: Further improves the fit by capturing additional complexity.

The model's performance is evaluated using \( R^2 \) scores and visualized with the best-fit curve.

### 5. Prediction for New Data
New data points (\( x \) values between -3 and 3) are generated, and predictions are made using the polynomial regression model. The results are plotted to show the predicted curve.

## Results
- **Simple Linear Regression**: Poor performance due to the quadratic nature of the data.
- **Polynomial Regression**:
  - **Degree = 2**: Significant improvement in accuracy, capturing the quadratic relationship.
  - **Degree = 3**: Further improvement, capturing additional nuances in the data.

## Code Structure
The repository contains the following steps:
1. Data generation and visualization.
2. Simple Linear Regression implementation.
3. Polynomial Regression with adjustable degree.
4. Model evaluation using \( R^2 \) scores.
5. Visualization of predictions for training, testing, and new datasets.

## Prerequisites
Ensure the following Python libraries are installed:
- pandas
- numpy
- matplotlib
- scikit-learn

To install the required libraries, run:
```bash
pip install pandas numpy matplotlib scikit-learn
