---
layout: post
title: (ENG) Backpropagation 
date: 2024-12-12
description: backpropagation
tags: backpropagation, DL
categories: study
featured: false
---
    
[Video Refrence](https://www.youtube.com/watch?v=tIeHLnjs5U8)


#### Before delving into specifics..

1.Limitation of the Perceptron

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


2.How Backpropagation solved this issue?

Backpropagation solved these problems by enabling multi-layer networks to learn nonlinear decision boundaries.

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

##### A neural network consists of:

1. Layers with weights : $w$ and biases : $b$
2. Activation function : $f$
3. Ouput function : $\hat{y}$
4. Loss function : $\eta$

A single layer NN equation, where $x$ is the input :

- The goal is to minimize loss:

$$ \hat{y}\ = f(w⋅x+b)$$

$$\eta=Loss(\hat{y} ,y)$$

##### Chain Rule

The chain rule(연쇄법칙)

Given functions $f$ and $g$ that are both differentiable,

and a composite function $ F = f(g(x)) = f \circ g $

