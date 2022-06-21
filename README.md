## EXP NO:10
## DATE:
## Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Create the text image using cv2.putText.
### Step3:
Then create the structuring image for dilation/erosion.
### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.### Step5:
Plot the images using plt.imshow.
## Program:
```
Developed by : sri harish M
Registeration Number:212220230047
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," sri harish",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')
# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')
```
## Output:
### Display the input Image
![image](https://user-images.githubusercontent.com/75241366/169989292-4d609f9a-f99e-4278-a618-9fa0ec542000.png)
### Display the Eroded Image
![image](https://user-images.githubusercontent.com/75241366/169989604-95c5af69-759c-4c99-abe7-8ffe4ec6bab6.png)
### Display the Dilated Image
![image](https://user-images.githubusercontent.com/75241366/169989378-45a1fc5f-1f28-4c7e-b012-c473c0e199b8.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
