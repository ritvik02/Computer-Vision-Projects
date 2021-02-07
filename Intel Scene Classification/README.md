# Intel-Scene-Classification

## Details

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Intel%20Scene%20Classification/images/image_1.png)

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Intel%20Scene%20Classification/images/image_2.png)


## Explanation of the various approaches used

### 0. [Basic approach](https://github.com/ritvik02/Computer-Vision-Projects/tree/main/Intel%20Scene%20Classification/basic_approach/nb)

In this approach we don't do much. We stick to most of fastai's default data augmentations except switching off one or two which
don't make sense. We use ResNet34 as our pretrained model, find the learning rate and train for a few epochs. We manage to achieve
an accuracy of ~93%. In the following approches we try to improve upon this model (in terms of accuracy and confusion b/w certain classes)

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Intel%20Scene%20Classification/images/image_3.png)


### 1. [Different architectures](https://github.com/ritvik02/Computer-Vision-Projects/tree/main/Intel%20Scene%20Classification/different_models/nb)

In this approach, we follow the exact same steps that we used in the basic approach except this time, 
instead of only trying ResNet34, we also try ResNet50 and ResNet101.

**ResNet50**

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Intel%20Scene%20Classification/images/image_4.png)

**ResNet101**

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Intel%20Scene%20Classification/images/image_5.png)


### 2. [Progressive image resizing](https://github.com/ritvik02/Computer-Vision-Projects/tree/main/Intel%20Scene%20Classification/progressive_image_resizing/nb)

Experiments have shown that if we train our model with lower resolution images and then use those weights to train our model with higher resolution images, our accuracy improves. 
And this is what we’ve tried in our second approach.

Results below:

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Intel%20Scene%20Classification/images/image_6.png)







