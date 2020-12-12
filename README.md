# Social-Distancing-Detector
Social Distance Detection, a Deep learning Computer vision project with OpenCV

What is social distancing?
Social distancing implies that people should physically distance themselves from one another, reducing close contact, and thereby reducing the spread of a contagious disease (such as coronavirus).

## Using OpenCV, computer vision, and deep learning for social distancing

We can use OpenCV, computer vision, and deep learning to implement social distancing detectors.
 The steps to build a social distancing detector include:

1. Apply object detection to detect all people (and only people) in a video stream.
2. Compute the pairwise distances between all detected people
3. Based on these distances, check to see if any two people are less than N pixels apart

For the most accurate results, we calibrate our camera through intrinsic/extrinsic parameters so that we can map pixels to measurable units.
An easier alternative (but less accurate) method would be to apply triangle similarity calibration which is what I have applied.

Both of these methods can be used to map pixels to measurable units.

For the sake of simplicity, our OpenCV social distancing detector implementation will rely on pixel distances.

# The implementation worked by:

- Using the YOLO object detector to detect people in a video stream
- Determining the centroids for each detected person
- Computing the pairwise distances between all centroids
- Checking to see if any pairwise distances were < N pixels apart, and if so, indicating that the pair of people violated social distancing rules

Furthermore, by using an NVIDIA CUDA-capable GPU, along with OpenCV’s dnn module compiled with NVIDIA GPU support, our method was able to run in real-time, making it usable as a proof-of-concept social distancing detector.

#### Github usually doesn't support files larger than 25 Mb.You can find the yolo weights in [My google drive](https://drive.google.com/file/d/1QrGGrZl-K2z9IH410o9oeGvbKdIDjGIS/view?usp=sharing) 
* Download it & move to yolo-coco folder.
