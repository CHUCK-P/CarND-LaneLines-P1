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

1) Do a color selection step.  For a variety of backgrounds and lighting conditions, this may be the hardest steps.  Thresholding is difficult.

2) Mask off early to eliminate extra processing

3) Convert the gray image to grayscale

4) Next I did a gaussian blur to remove artifacts

5) Do the Canny Edge Detect and set the gap and length parameters to ...

6) Do the Hough transform to find meaningful edges.  Draw lines within this step for the black mask overlay.

7) Do the line overlay by setting the alpha of a black-masked line image and merging to the oringinal





### 2. Identify potential shortcomings with your current pipeline

I've identified three potential shortcomings:
1) Lighting varies depending on the time of day, time of year, and weather conditions.
2) The lane lines might fall outside of the masked zone and not be picked up, correctly.
3) Color space is hard to predict, so setting the RGB thresholds is unreliable



### 3. Suggest possible improvements to your pipeline

1)  Implement an auto-thresholding routine.  Either an ambient light sensor or an averaging function could be sued to compensate.

2)  Use the Hough transform output to determine where the masking should be.