---
layout: post
title: (ENG) Training and Evaluating Deep Networks
date: 2024-12-17
description: 
tags: DL
categories: study
featured: false
---

#### Training and Evaluating Deep Networks

When dealing with DL, the following components are vital
1. training set
2. test set
3. validation set : used to tune a model's hyperparameters for model selection. Also, it prevents overfitting by early stopping


##### Hyperparameter Tuning
Hyperparameters in DL are usually tuned heuristically by hand or using grid search.

##### Dropout
Dropout is a form of regualization that randomly deletes units and their connections during training.

Pros
- 과적합 방지, 뉴런간의 의존성을 줄여 학습된 모델의 일반화 성능 향상
- 간단한 구현

Cons
- Additional overhead : 훈련 중에 매번 mask를 생성하고 적용
- 학습 속도 감소


##### Unsupervised Pretraining
This method can be useful when the volume of labeled data is small relative to the model's capacity.

- 딥러닝 초기의 학습 안정화와 데이터 부족 문제를 해결하기 위해고안된 기법