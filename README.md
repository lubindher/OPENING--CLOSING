# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

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
Use Opening operation.
### Step5:
Use Closing Operation.
 
## Program:
# Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'ALDRIN LIJO J E', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
# Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```python
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
# Use Closing Operation
```python
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2023-11-06 205000](https://github.com/lubindher/OPENING--CLOSING/assets/119559904/41f1bd18-af6c-4bed-a1a0-d389d7d3b7a3)


### Display the result of Opening

![Screenshot 2023-11-06 205024](https://github.com/lubindher/OPENING--CLOSING/assets/119559904/11ff6e5f-0e82-4606-8d2b-fc222b165575)


### Display the result of Closing

![Screenshot 2023-11-06 205038](https://github.com/lubindher/OPENING--CLOSING/assets/119559904/04643dbd-f842-46f8-b880-7984db09b41a)


## Result
Thus the Opening and Closing operation is used in the image using Python and OpenCV.
