Assignment 2: due Feb 10 (11:59 pm)
In this assignment, you will implement logistic regression. Then you will test your implementations on a small dataset.

Dataset: Use the same dataset as for the K-nearest neighbour in Assignment 1
Algorithm implementation: Implement logistic regression based on gradient descent and Newton's algorithm by filling in the functions in the skeleton code. The skeleton code consists of a Python Jupyter notebook:
Logistic regression skeleton: cs480_winter23_asst2_logistic_regression_skeleton.ipynb
Do not import any additional library. Feel free to run the Jupyter notebooks on any machine or Google Colab. Google Colab is a free cloud environment provided by Google that allows you to run Jupyter notebooks very easily. Python and all necessary libraries are already installed.
Submission via LEARN: Jupyter notebook
Results: Once you are done filling in all the functions, run the Jupyter notebook entirely and save the results. For the purpose of the assignment, use the default values included in the skeleton code for max_iters, gradient_norm_threshold and learning_rate. Make sure that the following results are saved:
Gradient descent (4 points):
Graph that shows the negative log probabilties based on 10-fold cross validation when varying the lambda hyperparameter from 0 to 25 in increments of 1.
The best lambda found by 10-fold cross validation and its cross validation negative log probability.
The test negative log probability and the test accuracy based on the best lambda
The number of iterations of gradient descent for the best lambda
Newton's algorithm (4 points):
Graph that shows the negative log probabilties based on 10-fold cross validation when varying the lambda hyperparameter from 0 to 25 in increments of 1.
The best lambda found by 10-fold cross validation and its cross validation negative log probability.
The test negative log probability and the test accuracy based on the best lambda
The number of iterations of Newton's algorithm for the best lambda
Discussion: At the end of the Jupyter notebook, add a text cell and answer the following questions:
Question 1 (2 points): Compare the results for gradient descent and Newton's algorithm. Discuss the scalability of each algorithm (i.e., time and space complexity). For what type of dataset would you use gradient descent versus Newton's algorithm?
Question 2 (2 points): Logistic regression finds a linear separator where as k-Nearest Neighbours (in Assignment 1) finds a non-linear separator. Compare the expressivity of the separators. Discuss under what circumstances each type of separator is expected to perform best. What could explain the results obtained with KNN in comparison to the results obtained with logistic regression?
Question 3 (3 points): Is the training set used in this assignment linearly separable? To answer this question, add some code to the Jupyter Notebook that uses a logistic regression classifier to determine whether the training set is linearly separable. Add some text that explains why this code can determine the linear separability of a dataset. Indicate whether the training set is linearly separable based on the results.
