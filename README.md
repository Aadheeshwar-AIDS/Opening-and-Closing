# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:Import the necessary packages.
<br>


### Step2:Create the Text using cv2.putText.
<br>

### Step3:Create the structuring element.
<br>

### Step4:Use Opening operation.
<br>

### Step5:Use Closing Operation.
<br>

 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
img1=cv2.putText(img,'AADHEESHWAR.A',(5,50),font,1.4,(255),5,cv2.LINE_AA)
plt.imshow(img1)

# Create the structuring element

Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)


# Use Closing Operation

image1=cv2.morphologyEx(img,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)



```
## Output:

### Display the input Image
<br>
<br>

![](IMG1.PNG)
<br>
<br>
<br>
<br>

### Display the result of Opening
<br>
<br>

![](IMG2.PNG)

<br>
<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>

![](IMG3.PNG)
<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.