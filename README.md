# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:
Create the Text using cv2.putText.
### Step3:
Create the structuring element.

### Step4:

Erode the image.

### Step5:

Dilate the image.

 
## Program:
```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((90,250),dtype='uint8')
img2=cv2.cvtColor(img1,cv2.COLOR_BGR2RGB)
font=cv2.FONT_HERSHEY_DUPLEX
cv2.putText(img2,'SHARMILA',(5,70),font,2,(218, 112, 214),3,cv2.LINE_8)
plt.imshow(img2)

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode1=cv2.erode(img2,kernel1)
plt.imshow(image_erode1)
# Dilate the image
image_dilate=cv2.dilate(img2,kernel1)
plt.imshow(image_dilate)
```
## Output:

### Display the input Image
![H1](https://github.com/Sharmilasha/EROSION-AND-DILATION/assets/94506182/ce9978c7-8549-41b8-978d-cb65e2884167)


### Display the Eroded Image
![H2](https://github.com/Sharmilasha/EROSION-AND-DILATION/assets/94506182/00a768b1-d4f6-49a4-aa24-6b04dbee8ca4)


### Display the Dilated Image
![h3](https://github.com/Sharmilasha/EROSION-AND-DILATION/assets/94506182/a009e900-0976-4eb4-a4ab-163ff005978f)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
