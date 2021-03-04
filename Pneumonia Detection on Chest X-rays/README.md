# Pneumonia detection

In this project, we use a pretrained model on a bunch of X-rays and try to predict whether the patient has Pneumonia or not.


![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Pneumonia%20Detection%20on%20Chest%20X-rays/image_4.png)

**Future scope**: Use stanford's CheXpert dataset and predict multiple diseases from the dataset

# [Mixed precision training](https://github.com/dipam7/fastai/blob/master/deep_learning/course1/lesson1/mixed-precision-on-pneumonia-using-fastai.ipynb)

In neural nets, all the floats i.e. our inputs, weights and activations are stored using 32 bits. Using 32 bits gives us a high amount of precision. But higher precision also means more computation time and more memory required to store these variables. We can also do these computations in half (FP16) or mixed precision (both). 

Results show that we've reduced the training time without much decrease in accuracy

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Pneumonia%20Detection%20on%20Chest%20X-rays/image_1.png)


![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Pneumonia%20Detection%20on%20Chest%20X-rays/image_2.png)
