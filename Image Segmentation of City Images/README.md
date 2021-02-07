# Image Segmentation of city Images

Image segmentation is an application of computer vision wherein we color-code every pixel in an image. Each pixel then represents a particular object in that image.
Image segmentation is usually used when we care about edges and regions, when we want to separate important objects from the background.

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Image%20Segmentation%20of%20City%20Images/image_3.png)

Image segmentation has a lot of significance in the field of medicine. Parts that need to be studied are color coded and viewed in scans taken from different angles. They are then used for things like automatic measurement of organs, cell counting, or simulations based on the extracted boundary information.

![Sample image](https://github.com/ritvik02/Computer-Vision-Projects/blob/main/Image%20Segmentation%20of%20City%20Images/image_2.png)

## Process
Treated image segmentation as a classification problem, where for every pixel in the image, we try to predict what it is. Is it a bicycle, road line, sidewalk, or a building? In this way we produce a color coded image where every object has the same color.

-	Executed by treating image segmentation as a classification problem by predicting what every pixel in the image is.
-	Used the U-net architecture as they perform better than GANs on applications like generating high resolution images from blurry images, thus color coded every pixel of an image using U-net. A U-Net then takes this and makes it bigger and bigger again and it does this for every stage of the CNN. However, constructing an image from a small vector is a difficult job. Hence we have connections from the original convolution layers to our deconvolution network.
-	Achieved an accuracy of 93.33%.

## Conclusion
Learnt how to color code every pixel of an image using a U-net. U-nets are gaining popularity because they’ve performed better than GANs on applications like generating high resolution images from blurry images. Hence it will be really useful to know what they are and how to use them.



