# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

### Orginal name:

```
NAME:Dharshini
Register number:212224230061
Exp name:Edge detection using Sobel, Laplacian, and Canny edge detectors.

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('bheem.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

```
# Sobel edge detector
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
# LAPLACIAN EDGE DETECTOR

```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

# CANNY EDGE DETECTOr

```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```




## Output:

### Orginal image :


<img width="614" height="569" alt="image" src="https://github.com/user-attachments/assets/c97b88a6-9334-4b91-8160-f260aa01326b" />


### SOBEL EDGE DETECTOR


<img width="619" height="572" alt="image" src="https://github.com/user-attachments/assets/be102de4-acbe-44cc-b1c1-8ac35096527f" />

### LAPLACIAN EDGE DETECTOR


<img width="648" height="573" alt="image" src="https://github.com/user-attachments/assets/a916880e-10b0-41db-a821-9f92188b2f58" />

### CANNY EDGE DETECTOR


<img width="662" height="578" alt="image" src="https://github.com/user-attachments/assets/092acb8a-9751-4407-8c14-07e8163fe695" />

## Result:

Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
