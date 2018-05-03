# Tensorflow101
--------

TensorFlow™ is an open source software library for high performance numerical computation. Its flexible architecture allows easy deployment of computation across a variety of platforms (CPUs, GPUs, TPUs), and from desktops to clusters of servers to mobile and edge devices. Originally developed by researchers and engineers from the Google Brain team within Google’s AI organization, it comes with strong support for machine learning and deep learning and the flexible numerical computation core is used across many other scientific domains.<br />
Starting in 2011, Google Brain built DistBelief as a proprietary machine learning system based on deep learning neural networks. Its use grew rapidly across diverse Alphabet companies in both research and commercial applications. Google assigned multiple computer scientists, including Jeff Dean, to simplify and refactor the codebase of DistBelief into a faster, more robust application-grade library, which became TensorFlow. In 2009, the team, led by Geoffrey Hinton, had implemented generalized backpropagation and other improvements which allowed generation of neural networks with substantially higher accuracy, for instance a 25% reduction in errors in speech recognition. TensorFlow is Google Brain's second generation system. Version 1.0.0 was released on February 11, 2017. While the reference implementation runs on single devices, TensorFlow can run on multiple CPUs and GPUs (with optional CUDA and SYCL extensions for general-purpose computing on graphics processing units). TensorFlow is available on 64-bit Linux, macOS, Windows, and mobile computing platforms including Android and iOS. TensorFlow computations are expressed as stateful dataflow graphs. The name TensorFlow derives from the operations that such neural networks perform on multidimensional data arrays. These arrays are referred to as "tensors". In June 2016, Dean stated that 1,500 repositories on GitHub mentioned TensorFlow, of which only 5 were from Google. In May 2016, Google announced its Tensor processing unit (TPU), an ASIC built specifically for machine learning and tailored for TensorFlow. TPU is a programmable AI accelerator designed to provide high throughput of low-precision arithmetic (e.g., 8-bit), and oriented toward using or running models rather than training them. Google announced they had been running TPUs inside their data centers for more than a year, and had found them to deliver an order of magnitude better-optimized performance per watt for machine learning. In May 2017, Google announced the second-generation, as well as the availability of the TPUs in Google Compute Engine. The second-generation TPUs deliver up to 180 teraflops of performance, and when organized into clusters of 64 TPUs, provide up to 11.5 petaflops. In February 2018, Google announced that they were making TPUs available in beta on the Google Cloud Platform. In May 2017, Google announced a software stack specifically for Android development, TensorFlow Lite, beginning with Android Oreo.

## Status
--------

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/codexponent/tensorflow101/master/LICENSE)

## Download and Installation
-------

To begin using this project, follow the following options to get started:
* Clone the repo: `git clone https://github.com/codexponent/tensorflow101.git`
* [Fork, or Download on GitHub](https://github.com/codexponent/tensorflow101)

## Usage
-------

- Fork or clone this repository and run on your IPython Notebook

## Features
--------

- Easy to learn topics with enough descriptions
- Clean code

## Code
--------


## <center>Tensorflow.</center>

##### TensorFlow™ is an open source software library for high performance numerical computation. Its flexible architecture allows easy deployment of computation across a variety of platforms (CPUs, GPUs, TPUs), and from desktops to clusters of servers to mobile and edge devices. Originally developed by researchers and engineers from the Google Brain team within Google’s AI organization, it comes with strong support for machine learning and deep learning and the flexible numerical computation core is used across many other scientific domains.

### <center>Importing Tensorflow</center>

##### To use TensorFlow, we need to import the library called tensorflow. We imported it with the name "tf", so the modules can be accessed by tf.moduleName


```python
import tensorflow as tf
```

### <center>Sessions</center>

##### Sessions are contex for creating a graph inside tensorflow. The graphs need session for the computaion of the values


```python
a = tf.constant(12)
b = tf.constant(13)
c = tf.multiply(12, 13)
```


```python
with tf.Session() as session:
    print(session.run(c))
```

    156
    

### <center>Matrix Multiplications</center>

##### As we all know, most of the images are just matrix tables, matrix tables of pixel values. So, most of the computer vision task relies on matrix multiplications of the matrices.


```python
matrixA = tf.constant([[3, 4], [4, 5]])
matrixB = tf.constant([[5, 6], [2, 3]])
matrixC = tf.matmul(matrixA, matrixB)

# Don't get confused with tf.multiply and tf.matmul as the first one does element wise multiplications 
# and the latter one gives the dot product of the two matrices
```


```python
with tf.Session() as session:
    print(session.run(matrixC))
```

    [[23 30]
     [30 39]]
    

### <center>Variables</center>

##### A TensorFlow variable is the best way to represent shared, persistent state manipulated by your program. Variables are manipulated via the tf.Variable class. A tf.Variable represents a tensor whose value can be changed by running ops on it.


```python
variableA = tf.Variable(0)
variableB = tf.constant(5)
activity1 = tf.assign(variableA, variableB)
```


```python
with tf.Session() as session:
    # To be able to use variables in a computation graph it is necessary to initialize them before 
    # running the graph in a session.
    session.run(tf.global_variables_initializer())
    session.run(activity1)
    print(session.run(variableA))
```

    5
    

### <center>Placeholders</center>

#####  A placeholder is simply a variable that we will assign data to at a later date. Unlike variables, the placeholders get's their data from outside of the computational graph.


```python
placeholder1 = tf.placeholder(dtype=tf.float32)
```


```python
with tf.Session() as session:
    print(session.run(placeholder1, feed_dict={placeholder1: 5}))
```

    5.0
    


```python
placeholder2 = tf.placeholder(dtype=tf.float32)
placeholder3 = tf.placeholder(dtype=tf.float32)
activity2 = tf.pow(placeholder2, placeholder3)
```


```python
with tf.Session() as session:
    activity3 = session.run(activity2, feed_dict={placeholder2: 2, placeholder3: 3})
    print(activity3)
```

    8.0
    

### <center>Thanks for completing this lesson!</center>

<hr>
##### Notebook created by: <a href="https://www.linkedin.com/in/sulabhshrestha/"> Sulabh Shrestha </a></h4> 
##### Github: <a href="https://github.com/codexponent"> CodeExponent </a>
##### Copyright &copy; 2018 [CodeExponent]

<hr>



## Documentation
--------

- The Full Documentation is available at (https://www.tensorflow.org/api_docs/)

## Contribute
----------

- Issue Tracker: https://github.com/codexponent/tensorflow101/issues
- Source Code: https://github.com/codexponent/tensorflow101
- Contributors: https://github.com/codexponent/tensorflow101/contributors.txt

## Support
-------

If you are having issues, please let us know.
I have a mailing list located at: sulabh4@hotmail.com

## References
-------

- https://en.wikipedia.org/wiki/TensorFlow
- https://www.tensorflow.org/api_docs/
- https://www.tensorflow.org

## Copyright and License
-------

Copyright 2018 Codexponent. Code released under the [MIT]license.

