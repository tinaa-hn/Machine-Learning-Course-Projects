Assignment 1: due Jan 27 (11:59 pm)

Part 1 (5 points): K-nearest neighbours

Download the dataset for K-nearest neighbours: knn-dataset.zip

Origin: this data is a modified version of the Optical Recognition of Handwritten Digits Dataset from the UCI repository. It contains pre-processed black and white images of the digits 5 and 6. Each feature indicates how many pixels are black in a patch of 4 x 4 pixels.

Format: there is one row per image and one column per feature. The class labels are 5 and 6. The label on line n in train_labels.csv is the label for the data point on line n in train_inputs.csv.

Implement k-nearest neighbours by filling in the functions in the skeleton code: cs480_winter23_asst1_knn_skeleton.ipynb

Do not import any additional library. Feel free to run the Jupyter notebook on any machine or Google Colab. Google Colab is a free cloud environment provided by Google that allows you to run Jupyter notebooks very easily. Python and all necessary libraries are already installed.

Once you are done filling in all the functions, run the Jupyter notebook entirely and save the following results:

A graph that shows the average accuracy based on 10-fold cross validation when varying the number of neighbours from 1 to 30.

The best number of neighbours found by 10-fold cross validation and its cross-validation accuracy.

The test accuracy based on the best number of neighbours

Upload to LEARN your Jupyter notebook with the results saved. Do not submit a zip file or pdf file. The TAs will run some of the Jupyter notebooks to verify the results.


Part 2 (5 points): Linear regression

Download the dataset for linear regression: regression-dataset.zip

Origin: this data consists of samples from a 2D surface that you can plot to visualize how linear regression is working.

Format: there is one row per data point and one column per feature. The targets are real values. The target on line n in train_targets.csv is the target for the data point on line n in train_inputs.csv.

Implement linear regression by filling in the functions in the skeleton code: cs480_winter23_asst1_linear_regression_skeleton.ipynb

Do not import any additional library. Feel free to run the Jupyter notebook on any machine or Google Colab. Google Colab is a free cloud environment provided by Google that allows you to run Jupyter notebooks very easily. Python and all necessary libraries are already installed.

Once you are done filling in all the functions, run the Jupyter notebook entirely and save the following results:

A graph that shows the average mean squared error based on 10-fold cross validation when varying the lambda hyperparameter from 0 to 3 in increments of 0.1.

The best lambda found by 10-fold cross validation and its cross validation mean squared error.

The test mean squared error based on the best lambda.

Upload to LEARN your Jupyter notebook with the results saved. Do not submit a zip file or pdf file. The TAs will run some of the Jupyter notebooks to verify the results.


Part 3 (5 points): Theory. In class, we discussed several loss functions for linear regression. However all the loss functions that we discussed assume that the error contributed by each data point have the same importance. Consider a scenario where we would like to give more weight to some data points. Our goal is to fit the data points (xn, yn) in proportion to their weights rn by minimizing the following objective: L(w) = Σn rn(yn − wTx̄n)2, where w is the vector of model parameters and (xn, yn) is a training data pair. To simplify things, feel free to consider 1D data (i.e., xn is a scalar).

Derive a closed-form expression for the estimate of w that minimizes the objective. Show the steps along the way, not just the final estimates.

Show that this objective is equivalent to the negative log-likelihood for linear regression where each data point may have a different Gaussian measurement noise. What is the variance of each measurement noise in this model?

Upload to LEARN a pdf file with your answers for the two previous questions.
