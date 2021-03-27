---
title: "Cat vs Non-cat Image Classification Using Deep Neural Network"
date: 2020-02-10 15:52:21
categories: DeepLearning Classification ComputerVision
badges:
  - type: warning
    tag: computer-vision
  - type: danger
    tag: cassification
image: "../../assets/img/cat-classification0.png"
---

In this assignment, I built an L-layer deep neural network for image classification. For here, L can be any integer greater than 0. In this case, I picked L as 5 and achieved training accuracy as 100% and test accuracy as 84% to differentiate cat and non-cat images.
Here is the representation of an L-layer deep neural network.

<!--more-->

![../../assets/img/cat-classification.png](../../assets/img/cat-classification.png)

![../../assets/img/cat-classification1.png](../../assets/img/cat-classification1.png)

The general deep learning methodology to build the model is as the following:

<ol>
<li>Initialize parameters / Define hyperparameters</li>
<li>Loop for num_iterations:</li>
<ul>
       <li>Forward propagation</li>
       <li>Compute cost function</li>
       <li>Backward propagation</li>
       <li>Update parameters (using parameters, and grads from backprop)</li><br>
</ul>
<li>Use trained parameters to predict labels</li>
</ol>
   
Here is the output of the cross-entropy cost after 2400 iterations.

![../../assets/img/cat-classification2.png](../../assets/img/cat-classification2.png)

The 5-layer neural network has test accuracy (84%) than your 2-layer neural network (72%) on the same test set.

Here is an example testing with a cat image.

![../../assets/img/cat-classification3.png](../../assets/img/cat-classification3.png)
