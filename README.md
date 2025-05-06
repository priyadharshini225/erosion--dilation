# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate  the image
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL


# Create the Text using cv2.putText
cv2.putText(img1,'Priya' ,(5,70),font,4,(255),2,cv2.LINE_AA)

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)

# Erode the image
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(10, 9))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output:

### Display the input Image
<br>![Screenshot 2025-05-06 094525](https://github.com/user-attachments/assets/7100a991-cb94-4e6c-8c9f-f4e56e34dbc6)

### Display the Dilated Image
<br>![Screenshot 2025-05-06 094532](https://github.com/user-attachments/assets/ed5b8375-065f-4f1b-b3f6-4a5d846b3856)

### Display the Eroded Image
<br>![Screenshot 2025-05-06 094538](https://github.com/user-attachments/assets/213c8dc9-eb9e-451d-b3cc-8963e75b4670)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
