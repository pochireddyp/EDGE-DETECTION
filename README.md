# EDGE-DETECTION
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

### program:

```p
Developed by:pochireddy.o
Reg.no:212223240115
```
### import the packages

```p
import cv2
import matplotlib.pyplot as plt
```

### Load the image, Convert to grayscale and remove noise

```p
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("bird.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR:

### SOBEL X AXIS:
```p
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dogpair.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL Y AXIS:

```P
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```

### SOBEL XY AXIS:

```P
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR

```P
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```


### CANNY EDGE DETECTOR
```P
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

### SOBEL X AXIS

![image](https://github.com/pochireddyp/EDGE-DETECTION/assets/150232043/c94e259a-1b61-4706-8082-adabb82ba01a)

### SOBEL Y AXIS

![image](https://github.com/pochireddyp/EDGE-DETECTION/assets/150232043/65b0208a-bd68-4141-8c78-6aa004d4827e)

### SOBEL XY AXIS

![image](https://github.com/pochireddyp/EDGE-DETECTION/assets/150232043/4803b567-ae6d-4fb8-ae41-dd58ad37f767)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/pochireddyp/EDGE-DETECTION/assets/150232043/9907cb31-fe87-4f3c-837d-3029e0b31656)


### CANNY EDGE DETECTOR

![image](https://github.com/pochireddyp/EDGE-DETECTION/assets/150232043/2e0be99a-5b96-42f0-bfae-6b12c58e16d5)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
