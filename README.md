# Ex.No 6: EDGE-DETECTION
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
### SOBEL EDGE DETECTOR
```
import cv2
import matplotlib.pyplot as plt

# Read the image using imread
img = cv2.imread('IMAGE2.webp')  # Replace with your image path
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)  # Convert the image to grayscale
gray = cv2.GaussianBlur(gray, (3, 3), 0)  # Apply Gaussian Blur

# Sobel X axis
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

# Sobel Y axis
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)  # Sobel for Y axis
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

# Sobel XY axis
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')  # Display Sobel XY result
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

```
### LAPLACIAN EDGE DETECTOR
```
# Laplacian Edge Detector
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(lap, cmap='gray')  # Display Laplacian result
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

```
### CANNY EDGE DETECTOR
```
# Canny Edge Detector
canny = cv2.Canny(gray, 120, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')  # Display Canny result
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/39b4bd40-f747-4994-9190-acf18080d1ab)

![image](https://github.com/user-attachments/assets/6dcb51eb-b897-494b-927e-27177830c880)

![image](https://github.com/user-attachments/assets/bc70915d-ede3-4567-bcc3-556946afa81c)



### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/ff612e0e-5960-4a76-866a-04b40fcd5f70)



### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/e2dd25ed-2e99-46eb-b154-4c733fcf0083)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
