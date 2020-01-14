# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg
[image2]: ./test_images_output/solidWhiteRight.jpg
[image3]: ./test_images_output/solidYellowCurve.jpg
[image4]: ./test_images_output/solidYellowCurve2.jpg
[image5]: ./test_images_output/solidYellowLeft.jpg
[image6]: ./test_images_output/whiteCarLaneSwitch.jpg

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of following steps.

Converting the images to grayscale
Applying Gaussian smoothing Module
Using Canny Edge Detection Module
Selecting the region of interest
Applying Hough Tranform line detection
Combining original image with Hough lines

In order to draw a single line on the left and right lanes, I modified the draw_lines() function first by segregating left and right lines by using slope. Negative slopes represent left side lines and positive are right lines. Then I averaged the lines and extrapolated them.

![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]
![alt text][image5]
![alt text][image6]


### 2. Identify potential shortcomings with your current pipeline


Potential shortcomings would be if the lanes are curvy, if there are any other lane markings and if the roads are very reflective.


### 3. Suggest possible improvements to your pipeline

Converting the image into darker scale to distinguish lane markings.
Improve the functionality to consider the curvy lanes.
