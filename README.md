# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale

### Step3:
Use Global thresholding to segment the image

### Step4:
 Use Adaptive thresholding to segment the image

### Step5:
Use Otsu's method to segment the image and display results.

## Program
### Name: MUKESH P
### Register number: 212222240068
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Otsu's thresholding
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

# Display the Otsu thresholding result
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()

# Read the Image and convert to grayscale
image = cv2.imread('VJK.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(image)
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Global thresholding to segment the image
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Adaptive thresholding to segment the image
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
                                    cv2.THRESH_BINARY, 11, 2)
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()


```
## Output

### Original Image

![WhatsApp Image 2024-10-16 at 16 09 25_f2c97fbb](https://github.com/user-attachments/assets/cf612649-78ec-4342-be31-95f8b424bbc9)



### Global Thresholding
![WhatsApp Image 2024-10-16 at 16 09 31_c80a48d2](https://github.com/user-attachments/assets/e7e98349-7698-4cec-8d7a-3ffed391eb2e)



### Adaptive Thresholding
![WhatsApp Image 2024-10-16 at 16 09 36_a5c7021e](https://github.com/user-attachments/assets/7b805a07-a62a-425f-9a95-b2bf6e6bddfd)




### Optimum Global Thesholding using Otsu's Method

![WhatsApp Image 2024-10-16 at 16 09 41_832ce7c0](https://github.com/user-attachments/assets/16a162ff-fcc8-4bc3-8345-2a847eb42d42)




## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
