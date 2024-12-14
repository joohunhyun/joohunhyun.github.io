---
layout: post
title: (ENG) Backpropagation 
date: 2024-12-12
description: backpropagation
tags: backpropagation, DL
categories: study
featured: false
---

**Table of Contents**
- [Introduction](#introduction)
  - [Limitations of the Perceptron](#limitations-of-the-perceptron)
  - [How Backpropagation Solved These Issues](#how-backpropagation-solved-these-issues)
- [The Chain Rule in Backpropagation](#the-chain-rule-in-backpropagation)
  - [Composition of a Neural Network](#composition-of-a-neural-network)
  - [The Chain Rule Explained](#the-chain-rule-explained)
- [Fitting the Curve](#fitting-the-curve-1)
- [What Is the "Best Curve"?](#what-is-the-best-curve-1)
- [Minimizing the Loss Function](#minimizing-the-loss-function-1)
  - [Methods:](#methods)
    - [References](#references)

<br>

#### Before delving into specifics..

##### Limitation of the Perceptron

a) Linear Separability

A single-layer perceptron uses a linear decision boundary to classify data.
It only functioned well if the data can be separated by a straight line (or hyperplane in higher dimensions).
However, some problems like XOR are not linearly separable.

b) Absence of Hidden Layers

The perceptron lacks hidden layers. Without them, it cannot model complex relationships between input features.

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


## Introduction

### Limitations of the Perceptron

1. **Linear Separability**  
   A single-layer perceptron uses a linear decision boundary to classify data.  
   While this works for linearly separable data, it fails for problems like XOR, which are not linearly separable.

2. **Absence of Hidden Layers**  
   Without hidden layers, the perceptron cannot model complex relationships between input features.

3. **Inability to Learn Nonlinear Functions**  
   The perceptron updates its weights using the rule:  
   $$w_i+1 = w_i + \eta(y-\hat{y})x$$  
   This works for linear problems but fails for nonlinear ones, as there’s no mechanism to capture nonlinear patterns.

### How Backpropagation Solved These Issues

Backpropagation (introduced by Hinton in 1986) addressed these limitations by enabling multi-layer networks to learn nonlinear decision boundaries:

1. **Nonlinear Activation Functions**  
   By introducing nonlinear activation functions (e.g., sigmoid, tanh, ReLU), backpropagation enables networks to learn complex, nonlinear relationships.

2. **Hidden Layers**  
   Hidden layers allow networks to transform inputs into hierarchical representations.  
   For example, in the XOR problem:  
   - The first hidden layer transforms inputs into a new feature space.  
   - The second layer uses this feature space to create a nonlinear decision boundary.

3. **Learning Complex Relationships**  
   Backpropagation uses the **chain rule** to compute gradients layer by layer, adjusting weights across all layers based on their contribution to output error.  
   This allows networks to learn mappings for nonlinear functions, solving problems like XOR.

---

## The Chain Rule in Backpropagation

### Composition of a Neural Network

A neural network (NN) consists of:

1. **Layers with Weights** ($$w$$) and **Biases** ($$b$$)  
2. **Activation Function** ($$f$$)  
3. **Output Function** ($$\hat{y}$$)  
4. **Loss Function** ($$\eta$$)

The equation for a single-layer NN, where $$x$$ is the input:  
$$\hat{y} = f(w \cdot x + b)$$  
The goal is to minimize the loss:  
$$\eta = Loss(\hat{y}, y)$$

### The Chain Rule Explained

The **chain rule** is the mathematical foundation of backpropagation:

1. For differentiable functions $$f$$ and $$g$$, let the composite function $$F = f(g(x)) = f \circ g(x)$$.  
2. Then, $$F'(x) = f'(g(x)) \cdot g'(x)$$.  
3. If $$t = g(x)$$, then:  
   $$\frac{dy}{dx} = \frac{dt}{dx} \cdot \frac{dy}{dt}$$  

This allows gradients to propagate backward through the network layer by layer.

---

## Fitting the Curve

In deep learning, fitting data points to a curve is a critical task. But what defines the "best curve"?

---

## What Is the "Best Curve"?

The "best curve" minimizes the **loss function**, which measures the total squared distance between the points and the curve.  

🧠 **Loss Function**: A function of multiple parameters $$\eta = (k_0, \dots, k_n)$$ that yields a single value.  
- A lower loss value indicates a better fit.

---

## Minimizing the Loss Function

How do we find the optimal parameters $$k_0, \dots, k_n$$ to minimize the loss function?

### Methods:
1. **Random Perturbation**: Randomly tweak the parameters.  
2. **Gradient Descent**: Predict the direction to minimize $$\eta$$ without brute-force calculations.



#### References

1. [Video Reference](https://www.youtube.com/watch?v=tIeHLnjs5U8)
2. [Blog Reference](https://evan-moon.github.io/2018/07/19/deep-learning-backpropagation/)
