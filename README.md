# Edge-Linking-using-Hough-Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary Python libraries which are required for the program.
<br>

### Step2:
Load a image using imread() from cv2 module.
<br>

### Step3:
Convert the image to grayscale.
<br>

### Step4:
Using Canny operator from cv2,detect the edges of the image
<br>

### Step5:
Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.
<br>


## Program:
```Python
import cv2
import numpy as np
img=cv2.imread('ber.jpeg',0)
cv2.imshow("GrayScale Image",img)


edges1 = cv2.Canny(img,100,200)

lines=cv2.HoughLinesP(edges1,1,np.pi/180, threshold=80, minLineLength=50,maxLineGap=250)


for line in lines:
    x1, y1, x2, y2 = line [0] 
    cv2.line(edges1,(x1, y1),(x2, y2),(255, 0, 0),3)


cv2.imshow('Hough',edges1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output

### Grayscale image
![Screenshot (16)](https://user-images.githubusercontent.com/94154941/234511083-595a15f4-d84e-4363-b267-bfb2548b8a9d.png)



### Display the result of Hough transform

![Uploading Screenshot (16).png…]()


## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 
