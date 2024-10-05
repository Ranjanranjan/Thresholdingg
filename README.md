# Thresholding

## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm
### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.


## Program

#### Name : Ranjan K
#### Register no : 212223230116


### Read and show the Original image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('/content/uiop.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
plt.show()

```
### Output:

<img width="406" alt="Screenshot 2024-10-05 at 11 37 07 AM" src="https://github.com/user-attachments/assets/db999a64-cf49-4ce3-b0e5-72d10a18b100">


### Convert the image to grayscale
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('/content/uiop.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()

```
### Output:
<img width="412" alt="Screenshot 2024-10-05 at 11 29 48 AM" src="https://github.com/user-attachments/assets/49596ca0-493f-4733-8af3-ce2007abc336">


### Use Global thresholding to segment the image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('/content/uiop.jpg')
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()

```
### Output:
<img width="410" alt="Screenshot 2024-10-05 at 11 30 13 AM" src="https://github.com/user-attachments/assets/06ea15b5-026f-4e6b-a89e-ef4c7de17e70">


### Use Adaptive thresholding to segment the image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('/content/uiop.jpg')
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()

```
### Output:
<img width="412" alt="Screenshot 2024-10-05 at 11 30 33 AM" src="https://github.com/user-attachments/assets/111d2c9c-b10a-4cfb-9369-6a996423e18a">


### Use Otsu's method to segment the image 
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('/content/uiop.jpg')
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()

```
### Output:
<img width="411" alt="Screenshot 2024-10-05 at 11 30 53 AM" src="https://github.com/user-attachments/assets/82aed1e8-d612-4224-bc8f-0fb43fa47112">


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
