# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## step1:
Import the required
## Step2:
Convert the input image to gray , to get more details and for laplcian operator, we have to convert input 
image to bgr format
## Step3:
Apply smoothing to reduce noise, here we are using gaussian blur
## Step4:
Perform the edge detector operation
## Step5:
Show to detected imag
 
## Program:


```
# Import the packages
import cv2
## Load the image, Convert to grayscale and remove noise
i=cv2.imread('WALT.jpg',-1)
gray=cv2.cvtColor(i,cv2.COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)
```
```
# SOBEL EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
sobel_x=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
cv2.imshow('sobel_x',sobel_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_y=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
cv2.imshow('sobel_y',sobel_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_xy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('sobel_xy',sobel_xy)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# LAPLACIAN EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
rgb_image = cv2.cvtColor(i,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(rgb_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# CANNY EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
canny_edges = cv2.Canny(img, 120, 150)
cv2.imshow('canny',canny_edges)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### SOBEL EDGE DETECTOR:
#### sobel_X:
![sobelx](https://github.com/Prethiveerajan/EDGEDETECTION/assets/94233064/161ed5bb-d221-4144-a20f-5dd6da9e06db)

#### sobel_Y:
![sobely](https://github.com/Prethiveerajan/EDGEDETECTION/assets/94233064/28e1a9af-7c27-4238-afcf-d5789d1fe1bb)

#### sobel_XY:

![sobelxy](https://github.com/Prethiveerajan/EDGEDETECTION/assets/94233064/a32da56d-c275-458a-8773-11565c87d2e4)


### LAPLACIAN EDGE DETECTOR:
![laplacianoperator](https://github.com/Prethiveerajan/EDGEDETECTION/assets/94233064/ef6284de-39b5-4752-94a9-1ee78d33f534)


### CANNY EDGE DETECTOR:
![canny](https://github.com/Prethiveerajan/EDGEDETECTION/assets/94233064/ad1cdf04-1d3e-45f8-852d-9c1fe82f86de)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
