#**Finding Lane Lines on the Road** 
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report1

Patrick Chiu.

[//]: # (Image References)

[image1]: ./test_images_output/gr_solidWhiteRight.jpg
[image2]: ./test_images_output/c_solidWhiteRight.jpg
[image3]: ./test_images_output/h_solidWhiteRight.jpg
[image4]: ./test_images_output/w_solidWhiteRight.jpg
[Readme]: ./ReadMe.md


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps. First, I converted the images to grayscale, then I .... 

![alt text][image1]

Use Gaussian reduce nosies, and converted by canny edge detection
![alt text][image2]

Set the ROI area & use Hough Transform to extract features
![alt text][image3]

Weight on source image
![alt text][image4]

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 

Step 1. Calculate slope of all lines.

Step 2. Base on slope , split lines to right and left

Step 3. linear regression to calculate the best fit for left and right line

Step 4. Find end points of left and right line, base on slope & left or right side

Step 5. convert end points from float to int type

Step 6. Draw left and right line.


If you'd like to include images to show how the pipeline works, here is how to include an image: 


### 2. Identify potential shortcomings with your current pipeline


one potential shortcoming would be unstable.
1. bounce on side of segment line 


### 3. Suggest possible improvements to your pipeline

Segment line consisted by dot and line.
So the end point is not always the same point as before, we can have a fix point on bottom. when scan a piece of line, change and draw.  
