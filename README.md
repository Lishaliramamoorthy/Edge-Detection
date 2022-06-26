## EX NO:07
## DATE:12.5.22
# <p align="center">Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale.

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image.

### Step6:
Using Canny operator from cv2,detect the edges of the image.
 
## Program:

``` Python
 Developed by:Lishali.R
 Register No:212220230028
# Import the packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Load the image, Convert to grayscale and remove noise
image1=cv2.imread('pras.jpg',0)
plt.imshow(image)
# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(image1,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(image1,cv2.CV_64F,0,1,ksize=5)
sobelxy= cv2.Sobel(image1,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.imshow(sobely,cmap='gray')
plt.imshow(sobelxy,cmap='gray')
# LAPLACIAN EDGE DETECTOR
dst = cv2.Laplacian(image1,cv2.CV_16S,ksize=3)
plt.imshow(dst,cmap='gray')
abs_dst = cv2.convertScaleAbs(dst)
plt.imshow(abs_dst,cmap='gray')
# CANNY EDGE DETECTOR
edges = cv2.Canny(image1,100,200)
plt.imshow(image1,cmap = 'gray')
plt.title('Original Image'), plt.xticks([]), plt.yticks([])
plt.imshow(edges,cmap = 'gray')
plt.title('Edge Image'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR


![1](https://user-images.githubusercontent.com/75237886/168734012-40e79e50-71d0-45f3-b11f-c025d9bd8979.png)

### LAPLACIAN EDGE DETECTOR

![2](https://user-images.githubusercontent.com/75237886/168734038-634cebc7-21e7-4fdb-8fd2-fcc551ee3f1a.png)



### CANNY EDGE DETECTOR


![3](https://user-images.githubusercontent.com/75237886/168734059-56539c14-7b9f-4c02-8420-d83c4afbad80.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
