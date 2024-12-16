---
layout: post
title: (KOR) Feature Selection, Extraction, and Ensamble Methods
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

##### 1. Boosting



##### 2. Bagging
- 가장 간단한 방법 - taking a vote(or weighted vote)
- In classification : 
- In numerical prediction : taking the average of all predictions


##### 3. Stacking