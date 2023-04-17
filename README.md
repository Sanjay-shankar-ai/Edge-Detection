### Edge-Detection
### Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

### Software Required:
Anaconda - Python 3.7

### Algorithm:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use any filters for smoothing the image to reduse the noise.

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
### Program:
``` 
# Import the packages and load the image, Convert to grayscale and remove noise:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("roger.jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```
```
# SOBEL EDGE DETECTOR:

# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("roger.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()
```
```
# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("roger.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()
```
```
# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("roger.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()
```
```
# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("roger.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()
```
```
# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("roger.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()
```
### Output:
### Intput Image:
![d1](https://user-images.githubusercontent.com/94231938/232530519-29c10cdd-0210-4c89-88b6-7400d3439afe.png)

### SOBEL EDGE DETECTOR:
### Sobel-x:
![d2](https://user-images.githubusercontent.com/94231938/232530572-04255b8e-b146-44aa-9461-8b4468b21480.png)

### Sobel-y:
![d3](https://user-images.githubusercontent.com/94231938/232530608-9b1bb4f9-d5a5-4157-9fe0-687b08b4169f.png)

### Sobel-xy:
![d4](https://user-images.githubusercontent.com/94231938/232530640-ac543bea-d7f1-4cf3-a853-25ca2ebb0419.png)


### LAPLACIAN EDGE DETECTOR
![d5](https://user-images.githubusercontent.com/94231938/232530691-f5a0dadd-4e7a-4d73-a21d-33e68f0da763.png)



### CANNY EDGE DETECTOR
![d6](https://user-images.githubusercontent.com/94231938/232530740-928fbacb-a71c-4c5d-bb27-a53cb55f9d44.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
