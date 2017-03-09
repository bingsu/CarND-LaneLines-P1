#**Finding Lane Lines on the Road** 

##Writeup 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
  * Make a pipeline that finds lane lines on the road
  * Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied Gaussian smoothing to reduce details
from the image.After that, I run the Canny Edge Detector and focus on a paticular area where that lane should appear.Later, I run Hough Line Detector to transform each edge x-y plane to slope intersect to find out the part of same line 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by seperating right/left according to slope. In other to extrapolate the lines, I used the extents of the mask applied on the image, calculated an average slope of the lines from Hough, and got new points for the edges of the image. However this method does not seem to work for the challenge question.



###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be the misbeahvior for challenge question.

Another shortcoming could be I wonder if we connected the line segment as shown in the project.How can a car differeciate solid and dashed line to perform different action? 

Last but not least, I doubt the usability of my solution for various use case. Since the chanllege question make it acting crazy and how bout under other road situation and various weather situation.


###3. Suggest possible improvements to your pipeline

A possible improvement would be to solidify line detection method. I will pick up more on computer vision and openCV beacause I know nothing about it before I start. When I have more tools in my hand, the accuracy will increase, I hope.

Another potential improvement could be to ...
