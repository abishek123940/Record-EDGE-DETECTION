# EXP 6. Record-EDGE-DETECTION

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Sobel operator** using OpenCV to detect edges.

### Step 5:
Apply **Prewitt operator** using custom kernels.

### Step 6:
Apply **Roberts operator** using custom kernels.

### Step 7:
Apply **Laplacian operator** using OpenCV.

### Step 8:
Apply **Canny edge detector** using OpenCV.

### Step 9:
Display all edge-detected images for comparison.

---

## Developed By

- **Name:** ABISHEK S
- **Register No:** 212224240003
  
## Program

### Step 1: Import Libraries and Load the Image
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('image.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### Step 2: Sobel Edge Detection

```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### Step 3: Laplacian Edge Detection


```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### Step 4: Canny Edge Detection

```python

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```



## Output
### Orginal Image

<img width="314" height="410" alt="download" src="https://github.com/user-attachments/assets/b78b1fcf-406a-46a7-b305-957c7e206690" />


###  Sobel Edge Detector

<img width="314" height="410" alt="download" src="https://github.com/user-attachments/assets/2ad00e83-8208-4271-bcf5-203c41431bef" />


###  Laplacian Edge Detector

<img width="314" height="410" alt="download" src="https://github.com/user-attachments/assets/a1443ca7-99e3-4884-a3a1-7c8cbb1faea5" />


###  Canny Edge Detector

<img width="314" height="410" alt="download" src="https://github.com/user-attachments/assets/e3ea200d-4c5b-41f3-bf34-876f0c32eef4" />





---

## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
