# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1: 
Import the necessary packages
### Step2: 
Give the input text using cv2.putText()
### Step3: 
Perform opening operation and display the result
### Step4: 
Similarly, perform closing operation and display the result
 
## Program:
```
DEVELOPED BY : PULI NAGA NEERAJ
REG.NO : 212223240130
```
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ASTROPHYSICIST',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image

![image](https://github.com/PuliNagaNeeraj/OPENING--AND-CLOSING/assets/138849173/c8c6591a-5c19-461e-aee0-d95a4081480c)


### Display the result of Opening

![image](https://github.com/PuliNagaNeeraj/OPENING--AND-CLOSING/assets/138849173/2dda6a18-a239-4c82-9536-9d8aff799e1d)

### Display the result of Closing

![image](https://github.com/PuliNagaNeeraj/OPENING--AND-CLOSING/assets/138849173/d7faa004-4b01-48c0-a59c-167bda249f86)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
