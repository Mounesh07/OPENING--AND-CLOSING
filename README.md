# OPENING-AND-CLOSING

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
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
### Import the necessary packages
```python
import cv2
import numpy as np
```

### Create the Text using cv2.putText
```python
# Create the original image with text
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'Hariharan A', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
small_img = cv2.resize(img, (700, 175))  # Resize dimensions as (width, height)
cv2.imshow('Original Image', small_img)
cv2.waitKey(0)
```

### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))  # Adjust size as needed
```

### Use Opening operation
```python
opening_img = cv2.morphologyEx(small_img, cv2.MORPH_OPEN, kernel)
cv2.imshow('Opening Operation', opening_img)
cv2.waitKey(0)
```

### Use Closing Operation
```python
closing_img = cv2.morphologyEx(small_img, cv2.MORPH_CLOSE, kernel)
cv2.imshow('Closing Operation', closing_img)
cv2.waitKey(0) # Final common
cv2.destroyAllWindows()
```

## Output:
### Display the input Image
![WhatsApp Image 2024-11-13 at 15 26 54_c740bbac](https://github.com/user-attachments/assets/7506b232-29c0-46a6-86cb-c9671394e549)


### Display the result of Opening
![WhatsApp Image 2024-11-13 at 15 31 21_2a7d6ed6](https://github.com/user-attachments/assets/15fee61c-bd5c-4d39-84d3-88c76215ee7a)


### Display the result of Closing
![image](https://github.com/user-attachments/assets/84d7417c-a8bf-4a92-aa4e-fe10bc63b190)


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
