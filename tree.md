---
title:  "How to implement seq2seq with Keras"
date:   2019-3-12
layout: single
author_profile: true
comments: true
tags:
---

![keras](/pics/keras/keras.png)

**Why do you need to read this?**



**Contents**

1. [](#SC)
2. [](#VO)
3. [](#FUNCTIONS)
4. [](#IO)
5. [](#CF)
6. [](#DS)
7. [](#LIBRARY)
8. [](#data)
9. [](#topics)
10. [Conclusion](#other)

## <a name="SC" ></a>1.

Decision Tree
- How DT decide which variable to split on. -> Entropy
- Can we quantify this into a metric
- Purity Metrics

- Gini
- Entropy

- Root Node
- Inner Node
- Leaf Node

- height 最大ノード数 from root to leaf
- depth

Inner Node is Question.
つまりノード内のトレーニングサンプルのクラスがより不純度が低くなるように分けていくわけです。

## <a name="VO" ></a>2.

```python

```

## <a name="FUNCTIONS" ></a>3.




## <a name="IO" ></a>4.




## <a name="CF" ></a>5.




## <a name="LIBRARY" ></a>7.



## <a name="data"></a>8.



## <a name="other"></a>10.

I hope it will be useful for you as well.

## References
- []()
- []()
- []()

# create sequences of images, input sequences and output words for an image
def create_sequences(tokenizer, max_length, descriptions, photos):
	X1, X2, y = list(), list(), list()
	# walk through each image identifier
	for key, desc_list in descriptions.items():
		# walk through each description for the image
		for desc in desc_list:
			# encode the sequence
			seq = tokenizer.texts_to_sequences([desc])[0]
			# split one sequence into multiple X,y pairs
			for i in range(1, len(seq)):
				# split into input and output pair
				in_seq, out_seq = seq[:i], seq[i]
				# pad input sequence
				in_seq = pad_sequences([in_seq], maxlen=max_length)[0]
				# encode output sequence
				out_seq = to_categorical([out_seq], num_classes=vocab_size)[0]
				# store
				X1.append(photos[key][0])
				X2.append(in_seq)
				y.append(out_seq)
	return array(X1), array(X2), array(y)
