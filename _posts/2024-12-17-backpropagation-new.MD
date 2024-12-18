---
layout: post
title: (ENG) Backpropagation - NEW
date: 2024-12-17
description: backpropagation
tags: DL
categories: study
featured: false
---


#### **Backpropagation**

Backpropagation is a method used in neural networks to adjust the weights and biases by minimizing the error (or loss) through gradient descent. It works by propagating the error backward through the network, layer by layer.

---

### **Steps of Backpropagation**

1. **Forward Pass**:
   - The input data is passed through the network, and the predicted output $$\hat{y}$$ is computed.
   - The loss (or error) is calculated using a loss function, e.g., Mean Squared Error (MSE):
     $$
     L = \frac{1}{2}(y - \hat{y})^2
     $$
     Where:
     - $$y$$: Actual target value.
     - $$\hat{y}$$: Predicted value.

2. **Backward Pass**:
   - Compute the gradient of the loss $$L$$ with respect to each weight and bias by applying the chain rule.

   For a single weight $$w$$, the gradient is:
   $$
   \frac{\partial L}{\partial w} = \frac{\partial L}{\partial \hat{y}} \cdot \frac{\partial \hat{y}}{\partial z} \cdot \frac{\partial z}{\partial w}
   $$
   Where:
   - $$z$$: Weighted sum before applying the activation function.

3. **Weight Update**:
   - Update the weights using the gradients and a learning rate $$\eta$$:
     $$
     w \leftarrow w - \eta \frac{\partial L}{\partial w}
     $$

---

### **Chain Rule Explanation**
The **chain rule** is the foundation of backpropagation. It allows us to calculate how a small change in one variable (e.g., weight) affects the loss by propagating through intermediate layers.

For example:
- If $$L$$ depends on $$a$$, and $$a$$ depends on $$b$$, then:
  $$
  \frac{\partial L}{\partial b} = \frac{\partial L}{\partial a} \cdot \frac{\partial a}{\partial b}
  $$

---

### **Key Points**
- Backpropagation calculates gradients layer by layer, starting from the output and moving backward to the input.
- The gradients tell us how to adjust each weight and bias to minimize the loss.
- It uses the chain rule of calculus to propagate the error backward through the network.

---

#### **Example**
Imagine a single-layer neural network with an activation function $$\sigma(z)$$:
1. Forward pass:
   $$
   \hat{y} = \sigma(w \cdot x + b)
   $$
   Loss:
   $$
   L = \frac{1}{2}(y - \hat{y})^2
   $$
2. Backward pass (for weight $$w$$):
   $$
   \frac{\partial L}{\partial w} = (y - \hat{y})(-\sigma'(z))(x)
   $$

3. Update the weight:
   $$
   w \leftarrow w - \eta \cdot \frac{\partial L}{\partial w}
   $$

---

### **Conclusion**

Backpropagation is essential for training neural networks, enabling them to learn from data by minimizing the error through gradient descent. It works by calculating and propagating the error backward to adjust the weights and biases efficiently.
