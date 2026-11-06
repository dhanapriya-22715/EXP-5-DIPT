# EXP-5-Ex.No:5 Implementation of filter
## Name: DHANAPPRIYA S
## Register No: 212224230056
# Aim

To apply various spatial filters (Average, Weighted Average, Gaussian Blur, Median Blur, and Laplacian filters) on an image using OpenCV and visualize the processed outputs.


# Procedure

1. **Import Libraries:** Import `cv2`, `numpy`, and `matplotlib.pyplot`.
2. **Read and Convert Image:** Load the input image (`photo.jpg`) and convert its color format from BGR to RGB.
3. **Apply Filters:**
* **Average Filter:** Create a standard 1D/2D smoothing kernel and apply it using `cv2.filter2D()`.
* **Weighted Average Filter:** Define a custom weighted kernel to preserve center pixel weight and apply it via `cv2.filter2D()`.
* **Gaussian Blur:** Use `cv2.GaussianBlur()` with a specified kernel size to smoothen the image with a Gaussian distribution.
* **Median Blur:** Use `cv2.medianBlur()` to effectively remove salt-and-pepper noise.
* **Laplacian Kernel / Operator:** Apply a Laplacian kernel using `cv2.filter2D()` or the direct `cv2.Laplacian()` function to highlight image edges and high-frequency variations.
4. **Display Results:** Plot the original image alongside each filtered output side-by-side using `matplotlib.pyplot` with axes turned off.
# Code:
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("photo.jpg")
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
# Output:

<img width="941" height="527" alt="image" src="https://github.com/user-attachments/assets/932cb830-ba2b-4338-9dc6-438a81d8e87d" />

<img width="896" height="440" alt="image" src="https://github.com/user-attachments/assets/ea8fab86-4309-404b-9f7c-d2fe07076e11" />

<img width="857" height="432" alt="image" src="https://github.com/user-attachments/assets/8cb063d8-b2bf-4c2b-9cfc-3daf42483f30" />

<img width="867" height="527" alt="image" src="https://github.com/user-attachments/assets/3dc33803-b412-46a3-98a3-de9ee1595355" />

<img width="840" height="432" alt="image" src="https://github.com/user-attachments/assets/85bf0716-21df-4e05-b9e0-a67a38f3aa66" />

<img width="845" height="425" alt="image" src="https://github.com/user-attachments/assets/1c0104fe-8ddb-4fd7-b566-2e61b9b3344e" />

# Result:
Thus To apply various spatial filters (Average, Weighted Average, Gaussian Blur, Median Blur, and Laplacian filters) on an image using OpenCV and visualize the processed outputs was verified successfully.



