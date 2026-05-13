# OPENING--AND-CLOSING
### Name - SANTHOSH KUMAR A
### Register Number - 212224230250
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:


## Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
## Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'SANTHOSH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
## Create the structuring element
```
kernel = np.ones((3, 3), np.uint8)
```
## Display the input image
```
print("SANTHOSH KUMAR")
print("212224230250")
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```

## Opening is erosion followed by dilation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
## Display the result of Opening
```
print("SANTHOSH KUMAR")
print("212224230250")
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```



## Closing is dilation followed by erosion
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Display the result of Opening
```
print("SANTHOSH KUMAR")
print("212224230250")
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')

```
# Output:

### Display the input Image


<img width="735" height="628" alt="image" src="https://github.com/user-attachments/assets/b19af6a5-a1fa-493f-ace6-e2501f2f3755" />


### Display the result of Opening
<img width="682" height="618" alt="image" src="https://github.com/user-attachments/assets/a4df14ca-81b9-4f33-a958-207f51bcb3ca" />



### Display the result of Closing

<img width="694" height="636" alt="image" src="https://github.com/user-attachments/assets/b8ad2689-f69a-4839-b9f8-a8277d6e54f1" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
