---
layout: post
title: (ENG) Feature Selection, Extraction, and Ensamble Methods
date: 2024-12-16
description: 
tags: ML
categories: study
featured: false
---
**Table of Contents**

---

#### Feature Subset Selection
Definition : Feature subset selection finds a subset of original features without new features

##### 1. Filter Method
- Evaluates features with performance measures based on information gain or distance between each attribute in the class
- 장점 : computationally siple and fast
- 단점 : slow searching
- 해결책 : use a single-attribute evaluator with ranking

##### 2. Wrapper Method
- Searches for best combination of features among **all** posttible combination
- 장점 : generally better performance, simple and direct
- 단점 : $$O(n^2)$$ time complexity - slow
- 해결책
  - eliminate irrelevant features
  - eliminate redundant attributes

##### 3. Embedded method
- Uses ML models for classification and then an obtimal subset of features/ranking of feature is built by the classifier algorithm


##### Search Methods
- Weka 예제에서는 classfier(wrapper, etc)와 search method 둘 다 정의해야한다.

##### Different Search Methods
1. Exhaustive : $$2^n$$ subsets
2. Backwards
3. Forwards
4. Bidirectional

<br>
---

#### Feature Extraction (AKA: Reducing Dimentionality)
Definition : extracts new set of features from the original features

##### PCA
- Definition : unsupervised approach to examine relations among a set of variables
- When to use this?
  - PCA is useful in reducing the dimentionality of  3-D, 4-D scatterplots (왜 사용하냐 : visually difficult to interpret data points in high-dimensional space)
- Ex : Compressing MNIST- dataset using PCA (to reduce dimension)


<br>
---

#### Ensamble Method
- Definition : 여러개의 모델들을 조합해서 더욱 정확한 결정을 내리는 방법 (위원회 운영과 비슷)
  
Types of Ensamble Methods:
1. Boosting
2. Bagging
3. Stacking

##### 1. Boosting :Ada-Boosting


##### 2. Bagging(stands for: Boostrap Aggrevating)
Bagging은 앙상블 기법들 가운데 가장 간단한 방법이다(taking a vote, or weighted vote). Decision Tree의 경우, training set에 따라서 그 구조가 매우 민감하게 바뀐다. 이런 경우에는 1) training set을 여러 개 만들고 2) 각각 모델을 만들어서 3) voting을 한다. In numerical prediction,  taking the average of all predictions.

Breiman(1996) noticed that an ensamble of trees improved when the trees differed significantly from each other, today called **Random Forest**. Bagging was able to create a diverse ensamble of classifiers by introducing randomness into the learning alg's input, which resulted in **better results**. In a DT, picking the best option can be randomized by picking one of the N best options at random instead of a signle winner (ex: top 3 options, top 5 options)

**Methods of picking different "winners" in bagging**
1. elite : picking the best one
2. randomization : picking 1 randomly from top 5 candidates
3. stochastic : top5 중에서 룰렛으로 고르는 방법 (weighted)

##### 3. Stacking
Stacking is used on models built by different learning algorithsm. For example, stacking can be used when you want to form a classifier for a given dataset with A) deicision tree inducer B) naive bayes learnner and C) instance based learning scheme.

Stacking involves a **metalearner** that replaces the voting procedure of boosing and bagging. Metalearner is used to discover how to best combine the output of the base learners to determine which classifiers are the reliable ones.

- base learners : level-0 models
- meta learner : level-1 model
- predictions from base models are inputs to the meta learner. (funnel처럼 위에서 아래로 내려온다)

TL;DR : Stackin combines predictions of base learners using metalearner(NOT voting)


![alt text](posts_/image.png)