# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

1. Convert the input image into grayscale
2. Run Gaussian Blur
3. Use Canny Edge to find all the edges
4. Zone out between leff and right lane for easier inspection of Hough Line result

draw_lines() modification
5. Use liner regression to find out best fit line from from Hough Line results
6. While we have the slope and Y can be determined, we can utilize liner equation to work out the required point of X
7. Draw overlay on images based on X and Y found



### 2. Identify potential shortcomings with your current pipeline

* The vertices of region of interest is a static region
* When the car is turning it can't find the outside lane correctly at all



### 3. Suggest possible improvements to your pipeline

* Based on the camera's field of view, distent and angel from the road to better calculate the region of interest in run-time
* Try to incorporate color in the lane finding pipeline

