# [Player and Football Detection]
Football as a sport alone is beautiful. It is like a blank canvas waiting to be filled by the players on the field. It is a stunning spectacle, where we see elegance and athleticism, coupled with skills and intelligence, all for the simple goal of putting the ball in the net. This is why it’s referred to as The Beautiful Game.
Added to that, we see the beauty of time and relativity on display in the sport. 2 minutes become 10, and 10 minutes become 2, depending on the score. Finally the desire and urge to compete and win which the players display and the fans embody, makes for a great spectacle.
For many centuries, the use of technology in football has been minimal, however seeing the advancements in the field of AI, one can already expect AI to be a very big part of Football.
From using Computer Vision for getting tracking data to using plotting libraries and machine learning algorithms to make sense of the data, there is a lot of potential for such advancements.
The current applications of AI that are being implemented in Football are Goal Line Technology (GLT), Video Assistant Referee (VAR), Electronic Performance and Tracking Systems(EPTS) and many more.

Objective - implementation of player and football detection using OpenCV, masking and contour techniques.

We use the France vs Belgium match clip as an example to perform player and football detection.

## Process
- Read the video frame by frame and convert them into HSV format.
The HSV format helps us to separate the background by their colour. Hence we will be able to separate the pitch from the rest of the players and then detect the players. Also, after detecting the players we will be able to identify the national team they are playing by their jerseys. 
- After specifying the ranges we first define a mask of green colour to detect the pitch.
- Then performed morphological closing operations on these frames. The closing operation will fill out the noise which is present in the crowd. So false detection can be reduced.
- The contours are a useful tool for shape analysis and object detection and recognition. We find contours on every frame. Hence to detect players we check for contours whose height is greater than the width. We will do the masking operation on the detected players for detecting their jersey colour, if the jersey colour is blue, we will put text as “France” and if it is red then we will put text as “Belgium”.
- We then detect the football using the same masking operations and save the images.


## Output
Video Output can be found on the drive link
https://drive.google.com/drive/folders/1oYMqZJwt6RKIKJIjZhkWiLY1qWE23n8m?usp=sharing

