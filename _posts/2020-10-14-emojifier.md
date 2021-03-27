---
title: "Using Word Vector Representations to Build an Emojifier"
date: 2020-10-14 12:23:51
categories: DeepLearning Keras
badges:
  - type: success
    tag: NLP
  - type: danger
    tag: LSTM
image: "../../assets/img/emojifier.png"
---

Using word vectors, even if my training set explicitly relates only a few words to a particular emoji, the algorithm will be able to generalize and associate words in the test set to the same emoji even if those words don't even appear in the training set. This allows us to build an accurate classifier mapping from sentences to emojis, even using a small training set.

<!--more-->

In this assignment, I built a sophisticated model (Emojifier-V2) that incorporates an LSTM neural network. Here is the overview of the model.

![../../assets/img/emojifier.png](../../assets/img/emojifier.png)

<hr>Layer (type)                 Output Shape          Param #   
<br>
input_1 (InputLayer)         (None, 10)            0         
<hr>
embedding_2 (Embedding)      (None, 10, 50)        20000050  
<hr>
lstm_1 (LSTM)                (None, 10, 128)       91648     
<hr>
dropout_1 (Dropout)          (None, 10, 128)       0         
<hr>
lstm_2 (LSTM)                (None, 128)           131584    
<hr>
dropout_2 (Dropout)          (None, 128)           0         
<hr>
dense_1 (Dense)              (None, 5)             645       
<hr>
activation_1 (Activation)    (None, 5)             0         
<br>
<br>
Total params: 20,223,927<br>
Trainable params: 223,877<br>
Non-trainable params: 20,000,050<br>
<br>
Finally, I got a test accuracy between 80% and 95%. If the training set were larger, the LSTM model would be much better than at understanding such complex sentences.
