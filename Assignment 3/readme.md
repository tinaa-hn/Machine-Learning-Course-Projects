Assignment 3: due March 3 (11:59 pm)
In this assignment, you will experiment with fully connected neural networks and convolutional neural networks, using the PyTorch package. PyTorch facilitates the design of neural networks, automatic differentiation and accelerated computation with GPUs and multi-core CPUs. Preliminary steps:



Familiarize yourself with PyTorch by going through the tutorial Get familiar with PyTorch: a 60 minute blitz
Download and install PyTorch on a machine with a GPU or use Google's Colaboratory environment, which allows you to run PyTorch code on a GPU in the cloud. Colab already has PyTorch pre-installed. To enable GPU acceleration, click on "edit", then "notebook settings" and select "GPU" for hardware acceleration. It is also possible to select "TPU", but the PyTorch code provided with this assignment will need to be modified in a non-trivial way to take advantage of TPU acceleration. Note that you can complete this assignment without any GPU (or TPU). Any computer that has several cores will also provide some degree of acceleration.


Download the base code for this assignment: cs480_winter23_asst3_cnn_cifar10.ipynb. (bug in the test function corrected on Feb 26: the test function now returns the averag_test_loss instead of the average_train_loss)
Answer the following questions by modifying the base code in cs480_winter23_asst3_cnn_cifar10.ipynb. Submit the modified Jupyter notebook via LEARN.



Part 1 (3 points) Architecture: Compare the accuracy of the convolutional neural network in the file cs480_winter23_asst3_cnn_cifar10.ipynb on the cifar10 dataset to the accuracy of simple dense neural networks with 0, 1, 2 and 3 hidden layers of 512 rectified linear units each. Run the code in the file cs480_winter23_asst3_cnn_cifar10.ipynb without changing the parameters to train a convolutional neural network. Then, modify the code in cs480_winter23_asst3_cnn_cifar10.ipynb to obtain simple dense neural networks with 0, 1, 2 and 3 hidden layers of 512 rectified linear units. Produce two graphs that contain 5 curves (one for the convolutional neural net and one for each dense neural net of 0-3 hidden layers). The y-axis is the accuracy and the x-axis is the number of epochs (# of passes through the training set). Produce one graph where all the curves correspond to the training accuracy and a second graph where all the curves correspond to the test accuracy. Train the neural networks for 10 epochs. Save the following results in your Jupyter notebook:

The two graphs for training and testing accuracy.

Add some text to the Jupyter notebook to explain the results (i.e., why some models perform better or worse than other models).


Part 2 (2 point) Activation functions: Compare the accuracy achieved by rectified linear units and sigmoid units in the convolutional neural network in cs480_winter23_asst3_cnn_cifar10.ipynb. Modify the code in cs480_winter23_asst3_cnn_cifar10.ipynb to use sigmoid units. Produce two graphs (one for training accuracy and one for test accuracy) that each contain 2 curves (one for rectified linear units and another one for sigmoid units). The y-axis is the accuracy and the x-axis is the number of epochs. Train the neural networks for 10 epochs. Save the following results in your Jupyter notebook:

The two graphs for training and test accuracy.

Add some text to the Jupyter notebook to explain the results (i.e., why one model performs better or worse than the other model).


Part 3 (2 points) Dropout: Compare the accuracy achieved with and without dropout in the convolutional neural network in cs480_winter23_asst3_cnn_cifar10.ipynb. Modify the code in cs480_winter23_asst3_cnn_cifar10.ipynb by inserting a dropout probability of 0.25 after each max pooling layer and a dropout probability of 0.5 after the hidden fully connected layer. Produce two graphs (one for training accuracy and the other one for testing accuracy) that each contain 2 curves (with and without dropout). The y-axis is the accuracy and the x-axis is the number of epochs. Produce curves for 20 epochs.

The two graphs for training and testing accuracy.

Add some text to the Jupyter notebook to explain the results (i.e., why did one model perform better than the other one).



Part 4 (2 point) Optimizers: Compare the accuracy achieved when training the convolutional neural network in cs480_winter23_asst3_cnn_cifar10.ipynb with four different optimizers: SGD (learning rate = 0.001), RMSprop (learning rate = 0.0001), Adagrad (default parameters) and Adam (default parameters). Modify the code in cs480_winter23_asst3_cnn_cifar10.ipynb to use the SGD, Adagrad and RMSprop optimizers. Produce two graphs (one for training accuracy and the other one for testing accuracy) that each contain 4 curves (for SGD, RMSprop, Adagrad and Adam). The y-axis is the accuracy and the x-axis is the number of epochs. Produce curves up to 10 epochs.

The two graphs for training and testing accuracy.

Add some text to the Jupyter notebook to explain the results (i.e., why did some optimizers perform better or worse than other optimizers).


Part 5 (3 points) Filters: Compare the accuracy of the convolutional neural network in cs480_winter23_asst3_cnn_cifar10.ipynb with a modified version that replaces each stack of (Conv2d, Activation, Max pooling) layers with 5x5 filters by a deeper stack of (Conv2d, Activation, Conv2d, Activation, Max Pooling) layers with 3x3 filters. Produce two graphs (one for training accuracy and the other one for testing accuracy) that each contain 2 curves (for 3x3 filters and 5x5 filters). The y-axis is the accuracy and the x-axis is the number of epochs. Produce curves up to 10 epochs.
The two graphs for training and testing accuracy.
Add some text to the Jupyter notebook to explain the results (i.e., why did one architecture perform better or worse than the other architecture).
Part 6 (3 points) Theory: Show that a neural network that uses the tanh activation function can represent the same space of functions as another neural network that uses sigmoid activation functions instead of tanh activation functions. More preciseley, let f(x) = W(1) tanh(W(2) x + b(2)) + b(1) be a two-layer neural network that uses the tanh activation function for the hidden layer. Design a mathematically equivalent neural network g(x) that uses the sigmoid activation function instead of tanh. Show that f(x)=g(x).
