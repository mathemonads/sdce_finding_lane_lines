# **Finding Lane Lines on the Road** 

## Writeup Template

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 

0. Take an image as input.


1. Convert to grayscale
2. Apply Gaussian noise
3. Apply the Canny transform to find the edges.
4. Apply an image mask using a manually identified region of interest.
5. Draw hough line segments.
6. Apply hough lines to original image

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

I don't think it would work if the lane markings are too far apart, possibly in different countries or on old roads.
As suggested by the Udacity reviewer, I could reduce lane shakiness by average using previous frames.

It would also work better on curved roads if I fit using a quadratic instead of a linear equation.


### 3. Suggest possible improvements to your pipeline

Fine-tune constants better.
