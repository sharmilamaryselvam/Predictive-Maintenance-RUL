# Aircraft Engine Predictive Maintenance using Machine Learning

## Project Overview

This project predicts the Remaining Useful Life (RUL) of aircraft engines using operational and sensor data.

The goal is to estimate how many cycles remain before engine failure and support proactive maintenance planning.

---

## Problem Statement

Aircraft engines degrade over time due to continuous operation.

Traditional maintenance methods either:

* perform maintenance too early
* or wait until failure occurs

This project builds a machine learning model to predict Remaining Useful Life (RUL) and support predictive maintenance decisions.

---

## Dataset

Dataset Used:
train_FD001

Dataset contains:

* Engine ID
* Cycle information
* Operational settings
* Sensor measurements

Target:

* Remaining Useful Life (RUL)

---

## Project Objective

Build a predictive maintenance system that:

* Predicts Remaining Useful Life (RUL)
* Identifies factors affecting engine degradation
* Supports maintenance planning
* Reduces unexpected failures

## Approach

1. Data Preparation
* Loaded training and testing datasets
* Removed unnecessary columns
* Handled constant features
* Prepared target variable (RUL)

2. Feature Engineering

* Created additional useful variables
* Selected relevant features

3. Model Development

Models trained:

* Linear Regression
* Random Forest Regressor
  
4. Hyperparameter Tuning

Applied GridSearchCV to optimize:

* Number of trees
* Tree depth
* Minimum split size
* Minimum leaf size
* 
5. Validation

Performed 5-fold cross validation to evaluate model stability.

---

## Results

Best Model:
Random Forest Regressor

Performance:

* Test R² = 0.9928
* Cross Validation Mean = 0.9942

Best Parameters:

* n_estimators = 200
* max_depth = None
* min_samples_split = 2
* min_samples_leaf = 1

Top Features:

* cycle
* sensor_11
* sensor_9
* sensor_4
* sensor_12

---

## Tech Stack

Python

Pandas

NumPy

Matplotlib

Scikit-learn

Joblib

---

## Business Insights
* Engine degradation follows nonlinear patterns.
* Sensor measurements provide strong predictive signals.
* Machine learning can estimate engine health before failure.
* Maintenance decisions can be scheduled proactively.

## Example Maintenance Rules:

* RUL > 50 → Healthy
* RUL 20–50 → Schedule Maintenance
* RUL < 20 → Immediate Maintenance

