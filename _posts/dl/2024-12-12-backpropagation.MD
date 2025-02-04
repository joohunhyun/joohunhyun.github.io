---
layout: post
title: (ENG) Backpropagation 
date: 2024-12-12
description: backpropagation
tags: DL
categories: study
featured: false
---

**Table of Contents**
- [Before delving in](#before-delving-in)
  - [Fitting the curve](#fitting-the-curve)
  - [What is the "best curve"?](#what-is-the-best-curve)
  - [Minimizing the loss function](#minimizing-the-loss-function)
    - [Limitation of the Perceptron](#limitation-of-the-perceptron)
    - [How Backpropagation solved this issue?](#how-backpropagation-solved-this-issue)
  - [Chain Rule behind Backpropagation](#chain-rule-behind-backpropagation)
    - [Composition of a NN](#composition-of-a-nn)
    - [Chain Rule](#chain-rule)
- [References](#references)

<br>

### Before delving in

#### Fitting the curve

#### What is the "best curve"?

Fitting data points across a plane using a curve is the most important question. 

So what is the "best curve"?

Loss function : Measure of total squared distance between the points and the curve

🧠 It is referred to as a **function** because it has multiple parameters $$ \eta = (k_0 ... k_5) $$

The function yields a sigle value, where low value = good fit

#### Minimizing the loss function

How can we find the best configuration of $$ (k_0 ... k_5) $$, or in other words, minimize the loss function?

Methods
Random pertubation : random changes to parameters

How can we make predictions to the value of $$\eta$$$ without performing all calculations via brute-force?

Gradient Descent Method


Sometimes the derivative is unknown (not derivable)


##### Limitation of the Perceptron

a) Linear Separability

A single-layer perceptron uses a linear decision boundary to classify data.
It only functioned well if the data can be separated by a straight line (or hyperplane in higher dimensions).
However, some problems like XOR are not linearly separable.

b) Absence of Hidden Layers

The perceptron lacks hidden layers. Without them, it cannot model complex relationships between input features.

c) Learning is not Incremental

Learning is not incremental over time - meaning it has no retention of previous learning.

c) Inability to Learn Nonlinear Functions

The perceptron updates its weights using a simple rule:

$$w_i+1=w_i + \eta(y-\hat{y})x$$

This works for linear problems but fails for nonlinear problems, as the perceptron has no mechanism to capture nonlinear patterns.


##### How Backpropagation solved this issue?

Backpropagation(1986, Hinton) solved these problems by enabling multi-layer networks to learn nonlinear decision boundaries.

a) Nonlinear Activation Functions

Backpropagation allows the use of nonlinear activation functions (e.g., sigmoid, tanh, ReLU).
Nonlinear activations enable the network to combine inputs in complex ways, effectively learning nonlinear decision boundaries.

b) Hidden Layers

Backpropagation trains networks with multiple layers of neurons (hidden layers).
Hidden layers allow the network to create hierarchical representations of data, transforming input features into complex, abstract representations.

For example, in the XOR problem:
1. The first hidden layer transforms the inputs into a new feature space.
2. The second layer uses this new space to create a nonlinear decision boundary.

c) Learning Complex Relationships

Backpropagation applies the chain rule to compute gradients layer by layer, allowing the network to adjust weights in all layers based on how they affect the output error.
This enables the network to learn mappings for nonlinear functions, solving problems like XOR.


#### Chain Rule behind Backpropagation

##### Composition of a NN

1. Layers with weights : $$w$$ and biases : $$b$$
2. Activation function : $$f$$
3. Ouput function : $$\hat{y}$$
4. Loss function : $$\eta$$

A single layer NN equation, where $$x$$ is the input :

- The goal is to minimize loss:

$$ \hat{y} = f(w \cdot x + b) $$

$$\eta=Loss(\hat{y} ,y)$$

##### Chain Rule

The **chain rule**(연쇄법칙)

1. Given functions $$f$$ and $$g$$ that are **both differentiable**, and a composite function $$ F = f(g(x)) = f \circ g $$
2. Then, $$ F'(x) = f'(g(x)) \circ g'(x)$$
3. If we assume $$ t=g(x) $$
4. Then, $$ \frac{dy}{dx} = \frac{dt}{dx} \cdot \frac{dy}{dt} $$



### References

1. [Video Reference](https://www.youtube.com/watch?v=tIeHLnjs5U8)
2. [Blog Reference](https://evan-moon.github.io/2018/07/19/deep-learning-backpropagation/)


