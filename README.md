# EX-6 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
### Step2:
Load a image using imread() from cv2 module.
### Step3:
Convert the image to grayscale
### Step4:
Using Sobel operator from cv2,detect the edges of the image.
### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY: Praveen D
REGISTER NUMBER: 212222240076
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("eagle.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:

![samurai](https://github.com/DINESH18032004/EDGE-DETECTION/assets/119477784/153921be-d89b-4248-87fc-2ee1e2dba4ca)

### SOBEL EDGE DETECTOR:
![Screenshot 2024-04-02 114529](https://github.com/DINESH18032004/EDGE-DETECTION/assets/119477784/1c121c40-51f5-413c-81aa-c17661196160)

![Screenshot 2024-04-02 114543](https://github.com/DINESH18032004/EDGE-DETECTION/assets/119477784/2b7cb9ca-7db2-43b5-ae34-4c594a8ca331)

![Screenshot 2024-04-02 114553](https://github.com/DINESH18032004/EDGE-DETECTION/assets/119477784/89e7aef1-6752-4a7e-9161-af85442b05af)

### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-04-02 114603](https://github.com/DINESH18032004/EDGE-DETECTION/assets/119477784/a70b62da-331d-4ad1-84ff-56a8895fd6b4)

### CANNY EDGE DETECTOR

![Screenshot 2024-04-02 114612](https://github.com/DINESH18032004/EDGE-DETECTION/assets/119477784/3c0126ea-800e-4922-a52e-e698564b8a37)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
