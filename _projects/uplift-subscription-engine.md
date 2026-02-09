---
layout:page 
title: "The Uplift Subscription Engine" 
description: "Predicting customer intervention effectiveness using CausalML.
---

## The Business Problem
A SaaS company is facing churn. Instead of a standard classification model, we are using **Uplift Modeling** to identify "Persuadables"—customers who only stay if given a discount.

## The Stats Behind the Model
We are estimating the **Conditional Average Treatment Effect (CATE)**:

$$\tau(x) = E[Y | X=x, T=1] - E[Y | X=x, T=0]$$

Where:
* $Y$ is the outcome (renewal).
* $T$ is the treatment (the discount).
* $X$ is the vector of customer features.

## Technical Stack
* **Language:** Python (Pandas, Scikit-Learn)
* **Causal Inference:** CausalML (Uber)
* **Deployment:** FastAPI & Docker