# Multi Label Classification of Satellite Images

In this project, we try to predict the multiple labels associated with satellite images. This is important for tracking human activities in large regions of the Earth, and conserving bio diversity.


## Process
- In the first step, we apply a number of transforms to our images. Why do we transform our images? We do it in order to give more variety to our data set and help our model learn well. If we are designing a face detection algorithm, we can randomly flip some images horizontally to get a better data set.
In case of satellites however, we can also flip the images vertically as satellite images have no orientation. The max_lighting and max_zoom parameters are set by trial and error to their best values.
max_warp will change the perspective of the picture. It is handy when it comes to data sets like pets and cars, which clearly can be viewed from different perspectives; you can look at the dog from atop, or on the same level when staying close to the ground and playing with it. But for satellite, it always views the ground from the same perspective–high up above the ground in the space. Thus, adding a perspective warp to the training data set will make it unrepresentative of real satellite images. Hence we turn it off.

- In the second step, we start by creating a random seed. This seed helps us create the same random data set (train / test split) every time and hence make our results reproducible. We then read the image list, split the labels using csv, create a 20% validation set, and split the multiple labels on white space.

- We download and use a pretrained model resnet50 (50 layers) that has been trained to identify thousands of categories of images.

- We use 2 metrics for our model. The first one is accuracy and the second one is f_score (which is used by Kaggle for this competition)

- Finally we set the learning rate, train a little, alter the learning rate and train some more. We can plot our training and validation losses.


## Result
- Achieved an accuracy of 95.97% and f_score of 93.08%.
- Secured 80th position on private leaderboard of Kaggle competition.

