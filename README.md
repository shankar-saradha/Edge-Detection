# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
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

 
## Program:

``` Python
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("image1.png")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

## SOBEL EDGE DETETCTOR:
### SOBEL X:

sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL Y:

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL XY:

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()


## LAPLACIAN EDGE DETECTOR:

laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()


## CANNY EDGE DETECTOR:

canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X

![download](https://user-images.githubusercontent.com/93978702/169323458-d78be9c6-7fad-43b6-8368-c3dfd86f468e.png)
<br>

#### SOBEL Y
![download](https://user-images.githubusercontent.com/93978702/169325557-014a2298-1266-4827-94b2-a37a0f1114c8.png)



#### SOBEL XY

![download](https://user-images.githubusercontent.com/93978702/169325775-ac4145f8-68ec-4712-8bc2-1ca953398fbd.png)

### LAPLACIAN EDGE DETECTOR
![download](https://user-images.githubusercontent.com/93978702/169325835-2ed126b2-a181-46c4-bc9e-98b8be48c1fc.png)

<br>


### CANNY EDGE DETECTOR
![download](https://user-images.githubusercontent.com/93978702/169325846-7e59ced8-50bd-4dfd-ba75-d2f1d92cafa6.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
