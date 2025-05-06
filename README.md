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
```
DEVELOPED BY: Samakash R S
REGISTER NO: 212223230182
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
def load_img():
    blank_img = np.zeros((600, 950), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='SAMAKASH', org=(50, 300), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=10, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img):
    fig=plt.figure(figsize=(12,10))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()

img = load_img()
display_img(img)
```
### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (12,12))
```
### Use Opening operation
```python
image=load_img()
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
display_img(opening_image)
```
### Use Closing Operation
```python
image=load_img()
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
display_img(closing_image)
```
## Output:

### Display the input Image

![alt text](<Screenshot 2025-05-06 090009.png>)

### Display the result of Opening

![alt text](<Screenshot 2025-05-06 085546.png>)

### Display the result of Closing

![alt text](<Screenshot 2025-05-06 085602.png>)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
