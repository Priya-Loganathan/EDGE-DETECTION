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
Convert the image to grayscale.

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Output:
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("rome.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
### SOBEL X AXIS
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
![325711014-d71caa4e-7186-4daf-86e1-d625bac041f4](https://github.com/Priya-Loganathan/EDGE-DETECTION/assets/121166075/1a9d89a6-01a8-4369-845c-dc48784d78eb)

### SOBEL Y AXIS
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
![325711607-c9c1dc89-1433-4cdc-80b0-2788166853c9](https://github.com/Priya-Loganathan/EDGE-DETECTION/assets/121166075/72e5dbdb-8163-42e6-b31b-85d47bb97532)

### SOBEL XY AXIS
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
![325711941-bc19a136-8cfe-468c-a135-1b01db6177c1](https://github.com/Priya-Loganathan/EDGE-DETECTION/assets/121166075/9e4d7b0f-f792-4e1a-a09b-36f0613ff425)

### LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
![325712689-6fa43c8d-074f-46b6-8222-8c533ea7f95e](https://github.com/Priya-Loganathan/EDGE-DETECTION/assets/121166075/1b76a493-2086-458d-a6c4-4c6f5db9c336)

### CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
![325712899-aa85bb65-5168-4bfc-81b9-db0e0406757a](https://github.com/Priya-Loganathan/EDGE-DETECTION/assets/121166075/5ae0c53b-a9d1-4dce-a5d7-cf6f2b4d8cf6)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
