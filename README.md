# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary pacakages
<br>

### Step2:
Create the text using cv2.putText
<br>

### Step3:
Create the structuring element
<br>

### Step4:
Erode the image
<br>

### Step5:
Dilate the Image
<br>

 
## Program:

```python
DEVELOPED BY : KULASEKARAPANDIAN K
REGISTER NO : 212222240052
```
### Import the necessary packages:
```python
import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


### Create the Text using cv2.putText:
```python
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"CARPE DIEM!",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```


### Create the structuring element:
```python
kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


### Erode the image:
```python
img_erode = cv2.erode(img,kernel1)
```



### Dilate the image:
```python
img_dilate = cv2.dilate(img,kernel1)
```

### Display Result:
```python
plt.imshow(img, cmap = 'gray')
plt.axis("off")

plt.imshow(img_erode, cmap = 'gray')
plt.axis("off")

plt.imshow(img_dilate, cmap = 'gray')
plt.axis("off")
```
## Output:

### Display the input Image:

![IMAGE](/ip.png)
<br>

### Display the Eroded Image:

![IMAGE](/erosion.png)
<br>

### Display the Dilated Image:

![IMAGE](/dilate.png)
<br>


## Result
Thus the generated text image is eroded and dilated using python and OpenCV..