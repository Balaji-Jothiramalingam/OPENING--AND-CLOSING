## Ex 10 - OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:
## Step 1:
Import the required libraries.

## Step 2:
Create a text image using cv2.putText().

## Step 3:
Define a structuring element (kernel) for the morphological operations.

## Step 4:
Apply the Opening operation using cv2.morphologyEx() with the cv2.MORPH_OPEN flag.

## Step 5:
Apply the Closing operation using cv2.morphologyEx() with the cv2.MORPH_CLOSE flag.

## Program:
Developed by : BALAJI J
Reg.no :212221243001
# Import the necessary packages
import cv2
import numpy as np
image = np.zeros((300, 700), dtype="uint8")

# Create the Text using cv2.putText
cv2.putText(image, 'Opening & Closing', (30, 150), cv2.FONT_HERSHEY_SIMPLEX, 2, (255, 255, 255), 5)

# Create the structuring element
kernel = np.ones((5, 5), np.uint8)

# Use Opening operation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

cv2.imshow('Input Image', image)
cv2.imshow('Opened Image', opened_image)
cv2.imshow('Closed Image', closed_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
## Output:
## Display the input Image

![image](https://github.com/user-attachments/assets/42c99dcb-fc2d-4847-8be5-7262e4559678)

## Display the result of Opening
![image](https://github.com/user-attachments/assets/da056158-8ae3-461a-baf0-dcbddb079a7d)


## Display the result of Closing
![image](https://github.com/user-attachments/assets/b139e26a-df93-4efa-8ecc-2f747a8b713e)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
