### EXP NO: 04
### DATE:

# <p align='center'> Histogram and Histogram Equalization of an image</p>
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.
### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
### Step3:
Display the histograms with their respective images.
### Step4:

Equalize the grayscale image.
### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: Saran M
# Register Number:212220230044
```
```python
# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image= cv2.imread('tiger.jpg')

Color_image= cv2.imread('lion.jpg') 
cv2.imshow('Gray image',Gray_image)

cv2.imshow ('colour image',Color_image)
cv2.waitKey()

# Display the histogram of gray scale image and any one channel histogram from color image
hist  = cv2.calcHist([Gray_image], [0], None, [256], [0,256]) 
histl=cv2.calcHist([Color_image], [1], None, [256], [0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.title("grey image")
plt.show()

plt.stem(histl)
plt.title("color image")
plt.show()
# Write the code to perform histogram equalization of the image. 
import cv2
Gray_image=cv2.imread('tiger.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image


![d1](https://user-images.githubusercontent.com/75235427/165107003-421dab6d-8b16-4ff4-975d-0ec9e4b471b2.jpg)


### Histogram of Grayscale Image and any channel of Color Image
![d2](https://user-images.githubusercontent.com/75235427/165107015-cb45c1a7-5c80-4ccb-be64-32a33955d13c.jpg)

### Histogram Equalization of Grayscale Image
![d3](https://user-images.githubusercontent.com/75235427/165107024-10fb5ed4-86f1-41b9-aa26-9efda6c37485.jpg)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
