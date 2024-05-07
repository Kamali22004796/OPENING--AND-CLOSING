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
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Datascientist',(5,70), font,2,(255),5,cv2.LINE_AA)


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

```
## Output:

### Display the input Image


![326241337-ecea916f-3d46-47e0-a0d1-3b2844b407eb](https://github.com/Kamali22004796/OPENING--AND-CLOSING/assets/120567837/5e5b4094-505a-4e93-b73b-696d1095593d)


### Display the result of Opening


![326241342-3a6027e5-f105-437e-a11f-b9e255ba32ae](https://github.com/Kamali22004796/OPENING--AND-CLOSING/assets/120567837/a45f2ea7-cf0c-475f-8373-0bb63f9a6cc7)


### Display the result of Closing

![326241354-eb44b501-9cdb-4871-bd38-8f40e9e2ffe1](https://github.com/Kamali22004796/OPENING--AND-CLOSING/assets/120567837/833076f8-232b-428f-83d0-be2ed625ad91)


## Result:

Thus the Opening and Closing operation is used in the image using python and OpenCV.


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
