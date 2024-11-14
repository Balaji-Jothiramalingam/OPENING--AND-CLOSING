## OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:
## Step1:
Import the necessary packages

## Perform opening operation and display the result

## Step4:
Similarly, perform closing operation and display the result

## Step5:
End the program

## Program:
Developed by :BALAJI J
Register number : 212221243001
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'DHONI',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis('off')


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")



# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
## Output:
## Display the input Image

![image](https://github.com/user-attachments/assets/03a66258-808c-47df-ac2c-0f3cfdbe2a29)


## Display the result of Opening

![image](https://github.com/user-attachments/assets/40ab690f-93cd-468a-9661-7e26c8d3a178)


## Display the result of Closing

![image](https://github.com/user-attachments/assets/930fc94d-9aca-4cc3-8ca8-ed7dc3fe0db2)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
