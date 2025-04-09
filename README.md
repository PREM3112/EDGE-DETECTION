# EDGE-DETECTION
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
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
## PREM.R
## 212223240124
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('istockphoto-486867874-1024x1024.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)  
sobel_edge = cv2.magnitude(sobel_x, sobel_y)
laplacian_edge = cv2.Laplacian(gray_image, cv2.CV_64F)
canny_edge = cv2.Canny(gray_image, 100, 200)
plt.subplot(2, 2, 2)
plt.imshow(laplacian_edge, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')


plt.subplot(2, 2, 3)
plt.imshow(canny_edge, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')

plt.subplot(2, 2, 4)
plt.imshow(sobel_edge, cmap='gray')
plt.title("Sobel Edge Detector")
plt.axis('off')

plt.tight_layout()
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR

![Screenshot 2025-04-09 090239](https://github.com/user-attachments/assets/33d2e07f-0c3a-4d52-a89d-3dd387c78a35)


### LAPLACIAN EDGE DETECTOR

![Screenshot 2025-04-09 090213](https://github.com/user-attachments/assets/22e91290-35e0-4fd7-a8b2-91613a671fd8)


### CANNY EDGE DETECTOR
![Screenshot 2025-04-09 090231](https://github.com/user-attachments/assets/3889fa55-7486-413e-ad93-2618647b8e5b)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
