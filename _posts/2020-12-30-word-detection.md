---
title: "Speech Recognition - Trigger Word Detection"
date: 2020-12-30 09:27:12
categories: DeepLearning Keras
badges:
  - type: success
    tag: NLP
  - type: danger
    tag: LSTM
image: "../../assets/img/worddetection1.png"
---

In this assignment, my trigger word is "Activate". Every time it hears you say "activate," it will make a "chiming" sound.
The model will use 1-D convolutional layers, GRU layers, and dense layers, which can be imported from Keras. The following figure shows the detail of the model.

<!--more-->

![../../assets/img/worddetection.png](../../assets/img/worddetection.png)

<hr>
Layer (type)                 Output Shape          Param #   
<hr>
input_1 (InputLayer)         (None, 5511, 101)     0         
<hr>
conv1d_1 (Conv1D)            (None, 1375, 196)     297136    
<hr>
batch_normalization_1 (Batch (None, 1375, 196)     784       
<hr>
activation_1 (Activation)    (None, 1375, 196)     0         
<hr>
dropout_1 (Dropout)          (None, 1375, 196)     0         
<hr>
gru_1 (GRU)                  (None, 1375, 128)     124800    
<hr>
dropout_2 (Dropout)          (None, 1375, 128)     0         
<hr>
batch_normalization_2 (Batch (None, 1375, 128)     512       
<hr>
gru_2 (GRU)                  (None, 1375, 128)     98688     
<hr>
dropout_3 (Dropout)          (None, 1375, 128)     0         
<hr>
batch_normalization_3 (Batch (None, 1375, 128)     512       
<hr>
dropout_4 (Dropout)          (None, 1375, 128)     0         
<hr>
time_distributed_1 (TimeDist (None, 1375, 1)       129       
<hr>
<br>
Total params: 522,561<br>
Trainable params: 521,657<br>
Non-trainable params: 904<br>
 <br>
Finally, the development set accuracy I got for the trigger word detection problem is 94.56%.
