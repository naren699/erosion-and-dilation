# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program
```py
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
img = np.zeros((300, 300), dtype=np.uint8)

# Insert text
cv2.putText(img, 'OPENCV', (30, 150),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, 255, 3)

# Create kernel
kernel = np.ones((5, 5), np.uint8)

# Apply Erosion
erosion = cv2.erode(img, kernel, iterations=1)

# Display images
plt.subplot(1, 2, 1)
plt.imshow(img, cmap='gray')
plt.title('Original Image')

plt.subplot(1, 2, 2)
plt.imshow(erosion, cmap='gray')
plt.title('Erosion')

plt.show()
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
img = np.zeros((300, 300), dtype=np.uint8)

# Insert text
cv2.putText(img, 'OPENCV', (30, 150),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, 255, 3)

# Create kernel
kernel = np.ones((5, 5), np.uint8)

# Apply Dilation
dilation = cv2.dilate(img, kernel, iterations=1)

# Display images
plt.subplot(1, 2, 1)
plt.imshow(img, cmap='gray')
plt.title('Original Image')

plt.subplot(1, 2, 2)
plt.imshow(dilation, cmap='gray')
plt.title('Dilation')

plt.show()
```
## Developed By

**Name:**  Narendhiran P

**Register No:**  212224230177

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

<img width="342" height="357" alt="image" src="https://github.com/user-attachments/assets/19304f33-a91d-4c74-aec3-12cf3d3238f9" />


### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

<img width="713" height="367" alt="image" src="https://github.com/user-attachments/assets/660e1bf5-fb8a-4057-b42e-90f6b0555707" />



### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="711" height="357" alt="image" src="https://github.com/user-attachments/assets/546b7ba0-7a3e-4420-b5d5-4a61e7834ad4" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
