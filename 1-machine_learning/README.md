<!-- PROJECT LOGO -->
<br />
<p align="center">
    <img src="../inputs/icons/learning.svg" alt="Logo" width="15% id="logo">
    <p  align="center" style="font-size:0.75em;">Icon made by <a href="https://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></p>
    <h1 align="center">Machine Learning overview</h1>
    <h2 align="center">Python Workshop - Leeds Institute for Data Analytics (LIDA)</h2>
</p>

The workshop has some additional materials:

1. [Presentation](#)
2. [Linear Regression notebook](Linear_regression.ipynb)
3. [Classification notebook](Classification.ipynb)
4. [Hidden Markov notebook](Hidden_Markov.ipynb)

## Necessary modules

* sklearn
* numpy
* pandas
* matplotlib.pyplot
* tensorflow
* tensorflow_probability

## General definitions

1. Artificial Intelligence:
    * The effort to automate intellectual tasks normally performed by humans.
    * Very good AI is a very good set of rules!
2. Machine Learning
    * Rather than giving the program the rules, an algorithm finds (figures out) the rules for us.
    * Classical programming: Data+rules = answers
    * ML: Data + answers = rules.
3. Neural networks
    * A form of machine learning that uses layered representation of data
    * a lot of layers

### Features

> Information that is given to the model (input).

### Labels

> Is what we are trying to predicting (output)

## TensorFlow

## TensorFlow useful methods

* `tf.Variable(itens, itens-type)`: return a tensor
* `tf.rank(tensor)`: return the tensor's rank
* `tf.shape(variable)`: return the tensor's shape
* `tf.zeros(shape)`: returns a tensor with values 0
* `tf.ones(shape)`: returns a tensor with values 1
* `tf.reshape(new-shape)`: returns a tensor with a different shape

### TensorFlow: core learning algorithms

* [Linear regression](https://www.tensorflow.org/tutorials/estimator/linear): It analyses the relationship between independent and dependent variables to make predictions.
* [Classification](https://www.tensorflow.org/tutorials/estimator/premade): It separates data points into separate categories.
* [Clustering](https://www.tensorflow.org/model_optimization/guide/clustering/clustering_comprehensive_guide): A way of grouping the data points into different clusters, consisting of similar data points.
* [Hidden Markov models](https://www.tensorflow.org/probability/api_docs/python/tfp/distributions/HiddenMarkovModel): The HiddenMarkovModel distribution implements a (batch of) discrete hidden Markov models where the initial states, transition probabilities and observed states are all given by user-provided distributions.