# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>


### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

 
## Program:
### Import the packages
``` Python
import cv2
import matplotlib.pyplot as plt
```
### Load the image, Convert to grayscale and remove noise
``` Python
image = cv2.imread('picture.jpg')
gray_image = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('Gray image',gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
img = cv2.GaussianBlur(gray_image,(3,3),0)
```
### SOBEL EDGE DETECTOR
``` Python
sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(1)
plt.imshow(sobelx,cmap ='gray')
plt.title('Sobelx image')
plt.xticks([])
plt.yticks([])
plt.show()
sobely = cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(1)
plt.imshow(sobely,cmap ='gray')
plt.title('Sobely image')
plt.xticks([])
plt.yticks([])
plt.show()
sobelxy = cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.imshow(sobelxy,cmap ='gray')
plt.title('Sobelxy image')
plt.xticks([])
plt.yticks([])
plt.show()
```
### LAPLACIAN EDGE DETECTOR
``` Python
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(1)
plt.imshow(laplacian,cmap ='gray')
plt.title('Laplacian image')
plt.xticks([])
plt.yticks([])
plt.show()
```
### CANNY EDGE DETECTOR
``` Python
canny_edges = cv2.Canny(img,120,150)
plt.figure(1)
plt.imshow(canny_edges,cmap ='gray')
plt.title('Canny_edges')
plt.xticks([])
plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/75235167/168247006-f720848a-9565-4833-a5c3-685aa3120e11.png)
![image](https://user-images.githubusercontent.com/75235167/168247823-048b13b4-ba76-4ddb-b398-8cd64433cc95.png)
![image](https://user-images.githubusercontent.com/75235167/168247118-c4062914-ae48-41a8-ad35-23a569780347.png)
### LAPLACIAN EDGE DETECTOR
![image](https://user-images.githubusercontent.com/75235167/168247210-44e55f71-c946-4e1f-8067-2aab440dfc30.png)
### CANNY EDGE DETECTOR
![image](https://user-images.githubusercontent.com/75235167/168247295-e8bd9ef5-a8f7-4308-ad65-47cc5bacf3f8.png)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
