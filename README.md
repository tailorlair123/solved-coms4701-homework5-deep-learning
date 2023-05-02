Download Link: https://assignmentchef.com/product/solved-coms4701-homework5-deep-learning
<br>
The objective of this homework is to build a hand gesture classifier for sign language. We will be using <u>​</u><u><a href="https://colab.research.google.com/">Google Colaboratory</a></u>​ to train our model (set up instructions at the end). The dataset will be in the form of csv files, where each row represents one image and its true label.

We have provided the skeleton code to read in the training and testing datasets. Before you begin coding, go through the provided code and try to figure out what each function is responsible for. Most of the functionalities are implemented in the ​<strong>SignLanguage</strong>​ class. Below are brief descriptions of each function and what is expected of you.




<ul>

 <li><strong>create_model</strong>​(self): You will generate a ​<u><a href="https://keras.io/models/sequential/">keras sequential</a></u><u>​</u> model here. Make sure to set the self.model variable with your compiled sequential model.</li>

 <li><strong>prepare_data</strong>​(self, images, labels): Mainly this splits the data into training and validation sets. You may choose to normalize or downsample your data here, as well.</li>

 <li><strong>train</strong>​(self, batch_size, epochs, verbose): This method invokes the training of the model. Make sure to return the generated history object. Your model will be trained for a max of 50 epochs during grading. Make sure you are using the input parameters (batch_size, epochs, verbose)</li>

 <li><strong>predict</strong>​(self, data): This method will be invoked with the test images. Make sure to downsample/resize the test images the same way as the training images, and return a list of predictions.</li>

 <li><strong>visualize_data</strong>(​ self, data): Nothing to do here. This is solely to help you visualize the type of data you are dealing with.</li>

 <li><strong>visualize_accuracy</strong>​(self, history): Nothing to do here. It plots out the accuracy improvement over training time.</li>

</ul>

Here are a few guides that may help you get started

<ul>

 <li><u><a href="https://keras.io/getting-started/sequential-model-guide/">Keras Guide: Getting started with the Keras Sequential model</a></u></li>

 <li><u><a href="https://cs231n.github.io/convolutional-networks/">Introduction to Convolutional Neural Networks (CNNs)</a></u></li>

 <li><u><a href="https://ujjwalkarn.me/2016/08/11/intuitive-explanation-convnets/">A practical guide to CNNs</a></u></li>

 <li>Check also the class slides on deep learning in the Lectures folder.</li>

</ul>

A few points to note:

<ul>

 <li>We will train each model for 30 epochs to ensure convergence. However, you are free to tune the batch_size hyperparameter.</li>

 <li>We require a ​<u><a href="https://towardsdatascience.com/train-validation-and-test-sets-72cb40cba9e7">train-validation split</a></u>​, but you are free to choose the dataset split ratio.</li>

</ul>

The following questions might help you better approach CNNs and Keras:

<ol>

 <li>What is one-hot encoding? Why is this important and how do you implement it in keras?</li>

 <li>What is dropout and how does it help overfitting?</li>

 <li>How does ReLU differ from the sigmoid activation function?</li>

 <li>Why is the softmax function necessary in the output layer?</li>

 <li>This is a more practical calculation. Consider the following convolution network:

  <ol>

   <li>Input image dimensions = 100x100x1</li>

   <li>Convolution layer with filters=16 and kernel_size=(5,5)</li>

   <li>MaxPooling layer with pool_size = (2,2)</li>

  </ol></li>

</ol>

What are the dimensions of the outputs of the convolution and max pooling layers?

<strong> </strong>

You will submit a README.txt or pdf file that should contain the following: –           Your name and UNI

<ul>

 <li>1-2 sentence answers to the questions above.</li>

 <li>A very brief explanation of your architecture choices, workflow or any relevant information about your model.</li>

</ul>




<h1>1.  Test-Run Your Code</h1>

Before you submit, make sure it works! Go to Runtime &gt; “Restart and run all…”. This will restart your kernel, clearing any set variables and run all cells again. This is to make sure your results are reproducible and do not depend on an overwritten variable!