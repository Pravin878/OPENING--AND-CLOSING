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
cv2.putText(img, 'pravin kumar G', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
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
![WhatsApp Image 2024-11-13 at 15 25 36_5a20d94d](https://github.com/user-attachments/assets/f06837c2-955e-4179-8ed1-04fcfadb7e43)



### Display the result of Opening

![WhatsApp Image 2024-11-13 at 15 25 57_29c1fb30](https://github.com/user-attachments/assets/3f7d9535-2209-4447-8625-4c2eaafc0b22)


### Display the result of Closing

![WhatsApp Image 2024-11-13 at 15 26 13_8b5c0041](https://github.com/user-attachments/assets/721da56f-6d87-40f1-820f-90df9157641b)


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
