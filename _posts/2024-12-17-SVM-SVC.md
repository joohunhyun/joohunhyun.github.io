---
layout: post
title: (ENG) SVM, SVC
date: 2024-12-16
description: 
tags: ML
categories: study
featured: false
---
**Table of Contents**

---

#### Classification Models
Definition : 두개의 class A and B를 feature space에서 분리하는 모델

- Decision Trees
- Probabilistic models
- Linear models
- Non-linear models

In the case of non-linear data, there are different methods to model this.

1. MLP : achieve non-linearlity by combining perceptrons(linear models)
2. SVM : supervised machine learning algorithm used for classification and regression tasks.
3. SVC : 


##### SVM

Support Vector Machine (SVM) is a supervised machine learning algorithm used for classification and regression tasks. The key idea is to find the best hyperplane that separates data points into different classes. In an ideal case, this hyperplane maximizes the margin between data points of different classes.

- Core Concepts:
  - The hyperplane is the decision boundary.
  - SVM focuses on data points (support vectors) near the decision boundary that influence its position.
  - The algorithm uses kernels to transform data into higher-dimensional spaces when it is not linearly separable in the original space.
- Applications: Image classification, text categorization, and other binary/multi-class problems.
- Pros: 
  - Effective for high-dimensional spaces.
  - Works well with a clear margin of separation.
- Cons:
  - Computationally expensive for large datasets.
  - Sensitive to the choice of kernel and hyperparameters.

###### RBF Kernel
The RBF kernel, also known as the Gaussian kernel, is one of the most commonly used kernels in SVM. It is a non-linear kernel that maps data points into a higher-dimensional space where a linear hyperplane can effectively separate them.

Characteristics:

- Non-linearity: It can model complex relationships in the data.
- Local influence: Points that are closer to each other have a higher similarity, and their influence decreases exponentially with distance
- Scalability: Effective for problems where the decision boundary is not linear.


- Pros:
  - Handles non-linearly separable data well.
  - Requires fewer hyperparameters compared to other kernels.
- Cons:
  - γ must be carefully tuned; poor tuning can lead to overfitting or underfitting.

###### Polynomial Kernel

The Polynomial kernel is another non-linear kernel used in SVM. It computes the similarity between two data points as a polynomial function of their inner product in the input space.

Characteristics:

- Non-linearity: Maps the input space to a higher-dimensional space defined by polynomial terms.
- Flexibility: The degree $$d$$ controls the complexity of the decision boundary.
- Global influence: Unlike the RBF kernel, it considers global features of the data.
- Pros:
  - Can model non-linear relationships with adjustable complexity via $$d$$
  - Effective for datasets where classes are distinguishable by polynomial decision boundaries.
- Cons:
  - More sensitive to feature scaling than the RBF kernel.
  - Higher degrees can lead to overfitting.


##### SVC

- SVC stands for Support Vector Classifier and is the implementation of SVM for classification tasks in libraries like scikit-learn.

- Key Differences Between SVM and SVC:
SVM is the broader concept that encompasses both classification and regression tasks (e.g., SVM for regression is called SVR).
- SVC is specifically the classification implementation of SVM in scikit-learn.
- Features of SVC:
  - It supports linear and non-linear kernels like polynomial, RBF (Radial Basis Function), and sigmoid.
  - Provides hyperparameters like C (regularization strength) and gamma (kernel coefficient) for tuning the model.


