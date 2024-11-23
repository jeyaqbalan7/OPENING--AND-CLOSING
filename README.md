# OPENING--AND-CLOSING->
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the structuring element

### Step3:
Use Opening operation

### Step4:
Use Closing Operation

## Program:
```
Developed BY : Pradeepraj P
Reg no : 212222240073
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
###  Create the structuring element
```
image = cv2.imread("ex-100.jpg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
### Use Opening operation
```
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
### Use Closing Operation
```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
## Output:

### Display the input Image
![download](https://github.com/user-attachments/assets/42d05e5c-0fb4-4bfd-a490-b7d92086514c)

### Display the result of Opening
![download](https://github.com/user-attachments/assets/c41231ea-6f5b-4cd9-a348-abe5c3f52b0b)

### Display the result of Closing
![download](https://github.com/user-attachments/assets/80bee1b6-44a7-4148-b19b-a92177af61f5)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
