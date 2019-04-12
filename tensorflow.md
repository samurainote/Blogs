---
title:  "Understanding Tensorflow: Regression and Classification"
date:   2019-3-23
layout: single
author_profile: true
comments: true
tags:
---

![keras](/pics/TensorFlow/tensorflow.png)
![model](/pics/TensorFlow/model.png)
![bord](/pics/TensorFlow/bord.png)
![copy](/pics/TensorFlow/copy.png)


**Why do you need to read this?**



**Contents**

1. [What is TensorFlow?](#SC)
2. [Pros and Cons of TensorFlow](#DS)
3. [WorkFlow of TensorFlow](#VO)
4. [Regression](#FUNCTIONS)
5. [Classification](#IO)
6. [Image Recognition](#CF)
7. [Conclusion](#other)


## <a name="SC" ></a>1. What is TensorFlow?

What is TensorFlow?

- Tensor: N-dimensional array
  - Vector: 1 dimension
  - Matrix: 2 dimensions

- Flow: data flow computation framework (like MapReduce)

- TensorFlow: a data flow based numerical computation framework
  - Best suited for Machine Learning and Deep Learning
  - Or any other HPC (High Performance Computing) applications

![flow](/pics/keras/flow.png)

## <a name="DS"></a>2


## <a name="VO" ></a>3. WorkFlow of TensorFlow

0. Data Preparation

1. Modeling
    - X: Define Placeholder
    - W: Define Variable
    - α: Define Activation Fanction
    - y: Define Neural Network

2. Loss Function
    - Define Error Function: tf.reduce_mean() ..
    - Define Validation Metrics: accuracy, confusion matrix..
    - Selection of Optimization Algorithm for Gradient Descent: tf.train.MomentumOptimizer()

3. Training
    - Set a session: tf.Session()


## <a name="FUNCTIONS" ></a>4. Regression

0. Import Library

```python
import numpy as np
import tensorflow as tf
```

1. Modeling

```python



```

2. Loss Function

```python



```

3. Training

```python



```

## <a name="IO" ></a>5. Classification



## <a name="CF" ></a>6. Image Recognition



## <a name="LIBRARY" ></a>7. Conclusion

We just quickly overviewed text preprocessing for seq2seq. I hope it will be useful for you as well.

## References
