# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:
Import the necessary modules.

### Step2:
For performing edge detection on a image.

Sobel
Laplacian
Canny

### Step3:
Display all the images with their respective edge detected images.

 
## Program:

``` 
# Import the packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread ('images.jpg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

# Load the image, Convert to grayscale and remove noise
plt.title('GRAY IMAGE')
plt.imshow(gray_image,cmap = 'gray')

img = cv2.GaussianBlur(gray_image,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray_image,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

# SOBEL EDGE DETECTOR
# sobelx
plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])
# sobely
plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])
# sobelxy
plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()

# laplacian
cv2.waitKey(0)
laplacian = cv2.Laplacian(gray_image,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()

# canny_edges
canny_edges = cv2.Canny(gray_image, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
![sobelx](https://user-images.githubusercontent.com/95388047/232011129-b5715216-3e50-4778-b21c-57e78057e1d3.jpg)

![sobely](https://user-images.githubusercontent.com/95388047/232011187-bcf414ab-41f5-4798-8205-ecaf8702b400.jpg)

![sobelxy](https://user-images.githubusercontent.com/95388047/232011063-20546ccd-1426-4480-a875-5ea385bf3242.jpg)

### LAPLACIAN EDGE DETECTOR

![lap](https://user-images.githubusercontent.com/95388047/232011234-db5f3e5b-4d2f-46cf-9e6f-cdffd39279e2.jpg)

### CANNY EDGE DETECTOR

![carry](https://user-images.githubusercontent.com/95388047/232011293-3616982b-eed7-4b79-b2f4-3e3e8b75cf49.jpg)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
