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

My pipeline consisted of 7 steps.

1) Make a copy of the original image to gray (grayscale image)

2) Convert the gray image to grayscale

3) Make a copy of gray to blur

4) Next I did a gaussian blur to remove artifacts

5) Did the Canny Edge Detect and set the gap and length parameters to ...

6) Do the Hough transform to find meaningful edges and set parameters to...

7) Next, I masked off the parts of the image that were not relevant

8) I then made a copy of Hough to lines

9) I then overlaid the lines onto the image

10) I then calculated the cost per frame as...

11) At 120fps, the total cost of the pipeline is ...


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

I've identified two potential shortcomings:
1) Lighting varies depending on the time of day, time of year, and weather conditions.
2) The lane lines might fall outside of the masked zone and not be picked up, correctly.


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...
Implement an auto-thresholding routine.  Either an ambient light sensor or an averaging function could be sued to compensate.

Another potential improvement could be to ...
Use the Hough transform output to determine where the masking should be.