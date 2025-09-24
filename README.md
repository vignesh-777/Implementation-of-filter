# ExNo: Implementation-of-filter
# Name:vignesh R
# Reg No:212223240177
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.


### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.
## Program:
```
 Developed By   : vignesh R
 Register Number: 212223240177
```

### 1. Smoothing Filters

## i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
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
## ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
## iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```
## iv)Using Median Filter
```
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
## i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
## ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters


## i) Using Averaging Filter
<img width="842" height="295" alt="image" src="https://github.com/user-attachments/assets/b9f3d4ea-034e-431f-9450-2a0dc47a1a34" />


## ii)Using Weighted Averaging Filter
<img width="600" height="427" alt="image" src="https://github.com/user-attachments/assets/53388730-a86f-445b-9db1-974c4e7b4c08" />

## iii)Using Gaussian Filter

<img width="620" height="441" alt="image" src="https://github.com/user-attachments/assets/88ad2046-3c92-4bbe-b999-b3b25130140d" />

## iv) Using Median Filter

<img width="622" height="438" alt="image" src="https://github.com/user-attachments/assets/02391d8b-fbae-4202-b49f-01efd3f19631" />

### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="682" height="442" alt="image" src="https://github.com/user-attachments/assets/717d24aa-aeea-45ae-86d4-a79daa96e426" />

## ii) Using Laplacian Operator
<img width="618" height="434" alt="image" src="https://github.com/user-attachments/assets/7a32213d-7e1b-40b1-b5fc-68718168e2a3" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
