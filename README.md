# Implementation-of-Erosion-and-Dilation
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
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:
'''
Developed by : S.Meena.
Registeration Number:212221240028.

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," MEENA",(5,70),font,2,(255),5,cv2.LINE_AA)
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
![Screenshot (42)](https://user-images.githubusercontent.com/94677128/169796528-0b4b4b6d-6b9c-4763-92b1-45689ad4fa3d.png)

### Display the Eroded Image
![Screenshot (43)](https://user-images.githubusercontent.com/94677128/169796899-d9b76364-4be0-47c4-9f7c-90edbf2b58f7.png)

### Display the Dilated Image
![Screenshot (44)](https://user-images.githubusercontent.com/94677128/169797189-a606a18c-df1c-4c9f-a7f0-b996a5f15af4.png)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
