# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1
Import the required libraries.

Step2
Convert the image from BGR to RGB.

Step3
Apply the required filters for the image separately.

Step4
Plot the original and filtered image by using matplotlib.pyplot.

Step5
End the program.



## Program:
### Developed By   : TRISHA PRIYADARSHNI PARIDA
### Register Number: 212224230293
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread(r"C:\Users\Trisha Priyadarshni\Downloads\Taj.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()



```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```
iv)Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()





```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()




```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![Screenshot 2025-04-28 090426](https://github.com/user-attachments/assets/23ff9abb-5643-492f-bcbd-cb6392d567cf)


ii)Using Weighted Averaging Filter
![Screenshot 2025-04-28 090431](https://github.com/user-attachments/assets/7c9155e2-c6a6-4151-8a32-ed433537d15e)


iii)Using Gaussian Filter
![Screenshot 2025-04-28 090437](https://github.com/user-attachments/assets/8b281f47-e7fb-496c-93d4-f623e3529b1d)

iv) Using Median Filter
![Screenshot 2025-04-28 090443](https://github.com/user-attachments/assets/e63fd55e-fb7e-4e81-9bc8-3111871547e3)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![Screenshot 2025-04-28 090515](https://github.com/user-attachments/assets/ce35b0eb-98cc-4e1c-aee6-f3d685cf5d2f)


ii) Using Laplacian Operator
![Screenshot 2025-04-28 090522](https://github.com/user-attachments/assets/ffb60e60-9c41-469e-8d51-d6b9917b07ea)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
