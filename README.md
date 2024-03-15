# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

### Developed By: VIGNESH KUMARAN N S
### Register Number: 212222230171

### Grayscale image and Color image
```py
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("dala2.jpeg")
color_image = cv2.imread("vijay.jpeg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale image and color image
```py
import numpy as np
import cv2
Gray_image = cv2.imread("dala2.jpeg")
Color_image = cv2.imread("vijay.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)```

### Histogram equalization of Grayscale image
```py

import cv2
gray_image = cv2.imread("dala2.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![og vijay](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/c7734556-8185-4d6d-9c9b-57707fe7548f)


![og dala](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/9332fa52-5cf2-40e9-9fdd-e4bb29b15bf8)




### Histogram of Grayscale Image and any channel of Color Image
### Grayscale image
![dala gray](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/f9fdb723-9f69-4907-992f-8c4f94543504)


![dala graph](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/95193e31-58d4-4359-9c51-eed71673bcb7)


### Color image
![thalapathy gray](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/dc92a010-5294-448f-ada8-ec21fd880647)

![thalapathy graph](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/c0df1ab8-05c8-491c-8a12-bd44a025f547)

### Histogram Equalization of Grayscale Image.
![dala gray 2](https://github.com/VigneshkumaranNS/Histogram-of-an-images/assets/119484483/df37e796-e722-4672-abf4-a7701ab4dba4)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
