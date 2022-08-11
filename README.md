# Filling-In-Missing-Data-With-Regression-Models

Missing Data

In this project we will use Regression Trees and Feature Map regression in order
to fill in missing data of an image. The goal of this problem is to train several models 
which interpolate the image at all pixels i ∈ [0, 253], j ∈ [0, 239].

One can think of this as a supervised learning problem as follows. Suppose 
y = f(x) := f(i, j) = imagess(i, j) be the pixel value of the image at position x = (i, j). 
Filling-in the missing values of the matrix can be thought of as a supervised learning problem 
where one learns the function f(x) = f(i, j) based on training on the available pixels and their
locations.

Let the training data ytrain, Xtrain consist of all available non-N/A pixel values and their
positions, while the testing positions Xtest be those of the missing pixels. Filling the
missing value of the matrix can then be thought as a supervised learning problem where
one learns the function f(i, j) which produces the pixel value as a function of location.

We take on the following tasks:

(a) Construct ytrain, Xtrain consisting of all available non-N/A pixel values and their
positions. Let Xtest be the positions of the missing pixels whose values we are
trying to reconstruct.

Next, using each of the following methods:
• RandomForrestRegresor
• GradientBoostingRegressor
• A 2 − D Gaussian kernel feature map regression

(b) Train a regression model via with 5−fold cross-validation over the training set
ytrain, Xtrain. Optimize parameters of our model so that we can minimize the
mean-squared cross validation error. 

(c) Predict yˆtest on Xtest and compute the MSE compared to the true pixel values ytest
at Xtest. Plot the completed images for each of our three optimal models in the
previous part.

(d) Investigate the effect of adding an L1 − L2 elastic net regularization to the 2D
Gaussian kernel feature map regression method and find the optimal parameters of
our model using cross-validation.

(e) One way to improve our model is to add new features as follows. Instead of
y = f(i, j), we could also consider the model y = f(i, j, yup, ydn, yl, yr) where
yup, ydn, yl, yr are the pixel values, if available, directly above, below, to the left
and to the right of the target pixel at i, j. Use −999 to denote a missing value
pixel. Repeat parts (a)-(c) with this new training set. 

Finally, we conclude which model produces the best MSE?
