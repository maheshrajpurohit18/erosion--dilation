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
Dilate the Image
## Program:
``` Python
Developed by : MAHESH RAJ PUROHIT J
Register Number : 21222240058
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'MAHESH',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![Screenshot 2024-05-05 164519](https://github.com/maheshrajpurohit18/erosion--dilation/assets/118749665/a6de343b-0b5c-4098-9416-721af4e5956f)



### Display the Eroded Image

![Screenshot 2024-05-05 164542](https://github.com/maheshrajpurohit18/erosion--dilation/assets/118749665/9b824eda-a8a5-43ca-b7a2-ac9adbaf5129)


### Display the Dilated Image

![Screenshot 2024-05-05 164558](https://github.com/maheshrajpurohit18/erosion--dilation/assets/118749665/feddca14-71c2-4b7d-9c44-7bbbb8f8d892)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
