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
