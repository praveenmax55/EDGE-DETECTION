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

![dipt 1](https://github.com/praveenmax55/EDGE-DETECTION/assets/113497509/a77a2d52-7fdf-4525-a113-a132a8eea8af)


### SOBEL EDGE DETECTOR:
![dipt 2](https://github.com/praveenmax55/EDGE-DETECTION/assets/113497509/7e5e6bd1-a9a1-4c02-8a52-97209e63ce00)

![dipt 3](https://github.com/praveenmax55/EDGE-DETECTION/assets/113497509/cfa52b96-5ecb-420d-bd89-1d1ca573bf57)

![dipt 4](https://github.com/praveenmax55/EDGE-DETECTION/assets/113497509/a582d59e-76e4-4efb-955c-a4051f395f17)



### LAPLACIAN EDGE DETECTOR

![dipt 5](https://github.com/praveenmax55/EDGE-DETECTION/assets/113497509/5a3be5ba-c811-46e0-8e73-982859fd912e)


### CANNY EDGE DETECTOR

![dipt 6](https://github.com/praveenmax55/EDGE-DETECTION/assets/113497509/d20523ae-a2b5-4520-ad8b-c90b8661afc7)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
