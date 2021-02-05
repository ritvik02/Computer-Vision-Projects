## Objective 

The objective of our project is to develop an Autonomous Fruit Harvesting robot.
This project is intended to help the farmers save their effort by making their work convenient which consequently increases productivity. Additionally, the idea of a Fruit Harvester will help save time spent on harvesting fruits and hence decreases the number of fruits that become inedible due to rotting.
The fundamental control system uses a camera module which detects the fruit from the surrounding. It then captures images and relays it over to the software. The software (computer vision algorithm) is designed to detect whether the particular fruit is ripe or not based on experimental data. If the fruit is ripe it sends over a signal to the robotic arm which then plucks the fruit.
This system is designed to help the farmers by easing their work and helping them by taking a small burden off their shoulders.

This repository showcases the computer vision part of the project which is currently under development. I have decided to approach the project with 2 methods. Method 1 dealing with image processing and method 2 dealing with neural networks, object detection algorithms with a little bit of pre and post processing applied in method 1.




## Method 1 - image processing using openCV

- Using kernel of 7 by 7, we applied median blur is used to reduce salt and pepper noise. We tried using different blurring techniques and found median blur as most appropriate.

-	To detect the colour, a mask is applied on the captured frame such that only the desired colour
i.e. colour of fruit is highlighted. The captured image is in the RGB colour space and is converted into the HSV colour space. This helps in highlighting the single colour and blocking all other colours from the image. The mask will be further divided into two types, one for the lower intensity levels and one for the higher intensity levels. We also used trackbar as an alternative approach to get the desired value of red in HSV.

-	For improving the accuracy of contours morphological transformation is used on the image. Applied morphological operation closing to remove holes inside fruit image. Applied morphological operation opening to remove external image noise.

- Since morphological transformation had a certain time lag in real time we used simple thresholding along with image dilation. dilation function is used to remove noise from the image.
This along with canny edge detection gave a output with negligible time lag in real time.

-	Applied Laplacian transform for edge detection. Other edge detection method were also used like Canny, SobelX, SobelY and Scharr for edge detection. Comparing results we saw Laplacian provided best results.  

-	In image processing detecting the shapes is done with the help of contours. Contours are basically all the points along the boundary of an object in the image with the same colour or intensity. Upon detecting the contours, the number of vertices play an important role in identifying whether the object of interest is a square or a rectangle or a circle. There is an available function in OpenCV to find contours in the image. The contours are points along the boundary and these are stored in the memory. We can define the contours by only the vertice points without storing all the pixels along the boundary, this process is used in almost all shape detection applications and is known as contour approximation.

-	minEnclosingCircle is used to find coordinates of center and radius of circle made on contour. drawContours() is used to draw contours. Contour only gets displayed if the area of contour is greater than or equal to threshold area, thus neglecting all small unnecessary contours in the image.


## Method 2 - Pre and post processing techniques + object detection algorithms (deep learning)
ongoing


## Deployment

As I plan on implementing this on a robotic arm which can potentially be deployed on a farm so for the deployment part, the model will be quantized i.e make it smaller to fit on small device like Raspberry pi. Once the fruit that needs to be harvested is successfully detected and classified as a 'Ripened fruit', the Arduino will pass a signal to the robotic arm to pluck the fruit.



