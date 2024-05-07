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

## PROGRAM:

 DEVELOPED BY:Divyadharshini.A
 
 REGISTER NUMBER: 212222240027

## IMPORT PACKAGES AND LOAD IMAGES
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dandelions.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
### SOBEL X:
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y:
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```

### SOBEL XY:
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```


## Output:
### ORIGINAL IMAGE:

![image](https://github.com/divyadharshiniddanbarasu/EDGE-DETECTION/assets/119393424/7b43d4fb-6b0c-4c7f-8c7c-417e83ca2672)

### SOBEL EDGE DETECTOR

![image](https://github.com/divyadharshiniddanbarasu/EDGE-DETECTION/assets/119393424/6327f7d9-f443-4764-9bad-d3462c057ad3)

![image](https://github.com/divyadharshiniddanbarasu/EDGE-DETECTION/assets/119393424/d03acd07-d975-439b-8a80-9b780687e3ac)

![image](https://github.com/divyadharshiniddanbarasu/EDGE-DETECTION/assets/119393424/e3c7435a-49f4-4ea7-8882-ad253b14e0d6)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/divyadharshiniddanbarasu/EDGE-DETECTION/assets/119393424/869e57c9-0eb7-4dc0-b067-af0451fd084d)



### CANNY EDGE DETECTOR
![image](https://github.com/divyadharshiniddanbarasu/EDGE-DETECTION/assets/119393424/71a10c81-3862-4c13-96a1-247f40e0865b)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
