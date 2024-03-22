# Histogram of images
## Aim
### To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
### Anaconda - Python 3.7

## Algorithm:
### Step1:
#### Read the gray and color image using imread()

### Step2:
#### Print the image using imshow().

### Step3:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
#### The Histogram of gray scale image and color image is shown.


## Program:

### Colour and Gray Image

# Developed By: YESHWANTH P
# Register Number: 212222230178
```py
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpeg")
color_image = cv2.imread("colour.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Histogram of Grayscale Image

```py
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpeg")
Color_image = cv2.imread("colour.jpeg")
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
```

### Histogram of Green channel of colour Image

```py
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```



```py

import cv2
gray_image = cv2.imread("gray.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:

### Input Grayscale Image and Color Image

![310936535-8a34d0fb-83f3-4282-9125-6ad34efbe3a2](https://github.com/Yeshwanthperumal/Histogram-of-an-images/assets/119476088/71588be0-f8cd-4442-8d5e-4a4a01cb4b0b)



### Histogram of Grayscale Image

![310936614-220a5e98-1730-4bd5-b487-c228dfc73243](https://github.com/Yeshwanthperumal/Histogram-of-an-images/assets/119476088/f6a1bb51-b0d2-4588-9104-cc67272621a1)


### Histogram of Green Channel of colour Image


![310936694-518cf597-c566-461a-8364-c76ff75ee609](https://github.com/Yeshwanthperumal/Histogram-of-an-images/assets/119476088/85122373-03ee-4c65-b228-8dd773878894)

### Histogram Equalization of Grayscale Image.


![310936783-5d3e5218-978f-4959-b188-b73ea886cb80](https://github.com/Yeshwanthperumal/Histogram-of-an-images/assets/119476088/c3ec5853-d1dc-4f55-96fd-7e4d94ed75a3)



## Result: 
### Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
