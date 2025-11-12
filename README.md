# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the required libraries.

### Step2:

Convert the image from BGR to RGB.

### Step3:

Apply the required filters for the image separately.

### Step4:

Plot the original and filtered image by using matplotlib.pyplot.

### Step5:

End the program.

## Program:
### Developed By   : LOGU R
### Register Number: 212224230141
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```PYTHON
import cv2
import numpy as np

# Load the image
image = cv2.imread("LOGU PASSPORT IMAGE.png")  # Replace with your actual image path
if image is None:
    raise ValueError("Image not found. Check the file path.")

# ------------------ 1. Averaging Filter ------------------
average_blur = cv2.blur(image, (5, 5))  # Kernel size (5x5)

# ------------------ 2. Weighted Averaging Filter ------------------
# Custom kernel (normalized)
kernel = np.array([[1, 2, 1],
                   [2, 4, 2],
                   [1, 2, 1]], dtype=np.float32)
kernel /= np.sum(kernel)
weighted_blur = cv2.filter2D(image, -1, kernel)

# ------------------ 3. Gaussian Filter ------------------
gaussian_blur = cv2.GaussianBlur(image, (5, 5), 0)

# ------------------ 4. Median Filter ------------------
median_blur = cv2.medianBlur(image, 5)  # Kernel size must be odd

# ------------------ Display Results ------------------
cv2.imshow("Original", image)
cv2.imshow("Averaging Filter", average_blur)
cv2.imshow("Weighted Averaging Filter", weighted_blur)
cv2.imshow("Gaussian Filter", gaussian_blur)
cv2.imshow("Median Filter", median_blur)

cv2.waitKey(0)
cv2.destroyAllWindows()


```

### 2. Sharpening Filters
```PYTHON

```
## OUTPUT:
### 1. Smoothing Filters
</br>
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/c6068449-d53f-42d2-bd86-43654d793231" />


i) Using Averaging Filter
</br>
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/752e6546-3c70-40b2-b887-026e88889e7c" />


</br>
</br>



</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
</br>

<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/2b9b0732-9376-4482-b264-eab35937c9a6" />

</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
</br>
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/0ff4ee0b-2272-4dae-906d-a6820f41d3a3" />

</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>

<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/294937be-8eab-4e06-879d-38cccb86c0bb" />

</br>
</br>

### 2. Sharpening Filters
</br>
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/f39a9617-9973-452c-b7ec-c8a015686345" />

i) Using Laplacian Kernal
</br>
</br>
</br>
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/7758aa91-0a30-49ef-8e5b-2947de2f91a4" />

</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br>

<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/7eb64106-5033-4f3c-b017-7dda06046bc6" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
