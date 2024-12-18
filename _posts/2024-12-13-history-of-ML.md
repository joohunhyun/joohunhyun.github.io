---
layout: post
title: (ENG) Brief History of AI
date: 2024-12-13    
description:
tags: ML, DL
categories: study
typograms: true
---

**Table of Contents**
- [1940s–1950s - Early Foundations](#1940s1950s---early-foundations)
- [1950s–1960s - Discovery of Neural Networks](#1950s1960s---discovery-of-neural-networks)
- [1970s–1980s - AI's First Winter(인공지능의 첫 겨울) \& Backpropagation(역전파기법)](#1970s1980s---ais-first-winter인공지능의-첫-겨울--backpropagation역전파기법)
- [1980s–1990s - Sequence Processing and Memory](#1980s1990s---sequence-processing-and-memory)
- [1997 - Long Short-Term Memory(LSTM) (Hochreiter \& Schmidhuber)](#1997---long-short-term-memorylstm-hochreiter--schmidhuber)
- [1980s–1990s - Visual Recognition and Spatial Data](#1980s1990s---visual-recognition-and-spatial-data)
- [2012 - Deep Learning Revolution](#2012---deep-learning-revolution)
- [2014 - Generative Adversarial Networks(GAN) (Goodfellow)](#2014---generative-adversarial-networksgan-goodfellow)
- [2017 - Attention Mechanisms and Transformers (Vaswani et al.)](#2017---attention-mechanisms-and-transformers-vaswani-et-al)
- [2020s - Multi-Modal AI and Real-Time Applications](#2020s---multi-modal-ai-and-real-time-applications)
- [TL;DR](#tldr)

---

#### 1940s–1950s - Early Foundations
Discovery: Boolean logic and the Turing Test

Problem: How can we formalize reasoning and test machine intelligence?

Solution: Alan Turing introduced the concept of a machine capable of computation (Turing Machine) and proposed the Turing Test as a way to determine if a machine exhibits intelligent behavior.

<br>

#### 1950s–1960s - Discovery of Neural Networks 

Discovery: Perceptron (1958, Frank Rosenblatt)

Problem: How can we mimic the human brain's ability to learn patterns?

Solution: The perceptron, a simple single-layer neural network, was developed to classify data linearly by adjusting weights using feedback. However, it was unable to solve non-linear problems, such as XOR.

<br>

#### 1970s–1980s - AI's First Winter(인공지능의 첫 겨울) & Backpropagation(역전파기법)

Discovery: Backpropagation (1986, Rumelhart, Hinton, Williams)

Problem: 
How can multi-layer neural networks be efficiently trained?

Solution: Backpropagation introduced a systematic way to compute gradients and update weights in deep networks using the chain rule, which is the cornerstone of deep learning.This allowed to solve  non-linear problems.Applications suggested during that period included image recognition and character classification but were limited by computational power and data availability.

<br>

#### 1980s–1990s - Sequence Processing and Memory 
Discovery: Recurrent Neural Networks(RNN) (1986, Rumelhart & McClelland)

Problem: How can sequential data be modeled and retain context from prior inputs?

Solution: RNNs introduced a feedback loop where outputs from previous steps are fed back as inputs, allowing networks to maintain a "memory" over time.

Limitations: RNNs faced vanishing gradient issues, making them ineffective for long sequences -> LSTM was introduced to resolve this issue.

<br>

#### 1997 - Long Short-Term Memory(LSTM) (Hochreiter & Schmidhuber)

Problem: How can we learn and retain long-term dependencies in sequences

Solution: LSTMs introduced gated cells to control the flow of information, solving vanishing gradient problems. Applications include speech recognition and language translation.

<br>

#### 1980s–1990s - Visual Recognition and Spatial Data

Discovery: Convolutional Neural Networks (CNNs, 1989, LeCun)

Problem: How to efficiently process and recognize spatially structured data like images.

Solution: CNNs use convolutional layers to detect patterns such as edges and textures by learning spatial hierarchies. Pooling layers reduce dimensionality while preserving critical information.

Applications: Handwritten digit recognition (e.g., MNIST dataset) and later extended to more complex tasks like object detection.

<br>

#### 2012 - Deep Learning Revolution

Discovery: Deep CNNs and AlexNet (2012, Krizhevsky, Sutskever, Hinton)

Problem: How to achieve state-of-the-art(SOTA) accuracy in image recognition.

Solution: AlexNet leveraged deeper architectures, ReLU activations, and GPUs for training, achieving a breakthrough in the ImageNet competition. (Previous SOTA classification : 74% -> Alexnet `84.69%`)

Applications: Facial recognition, autonomous vehicles, and medical imaging.

<br>

#### 2014 - Generative Adversarial Networks(GAN) (Goodfellow)

Problem: How can we generate new output data that resembles an input dataset?

Solution: GANs use a generator and discriminator in a competitive framework, enabling applications like image synthesis and style transfer.

<br>

#### 2017 - Attention Mechanisms and Transformers (Vaswani et al.)

Problem: How can we handle long-term dependencies and parallelize(병렬화) sequence processing?

Solution: The attention mechanism learns relationships between all inputs simultaneously, eliminating sequential constraints. Transformers like BERT and GPT revolutionized natural language processing (NLP).

Applications: Machine translation, summarization, and chatbots.

<br>

#### 2020s - Multi-Modal AI and Real-Time Applications

Discovery: Multi-Modal Models (e.g., CLIP, DALL-E)

Problem: How can we unify processing across different modalities like text, images, and audio?

Solution: Pretraining large-scale models that align multiple data types, enabling applications in creative AI and real-time analysis.

<br>

#### TL;DR

- Backpropagation solved problem of non-linearity.
- RNNs/LSTMs enabled handling sequential data.
- CNNs revolutionized image processing.
- Transformers led to breakthroughs in NLP and multi-modal AI.