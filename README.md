# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By:
### Register Number: 
i) #To Read,display the image
```
import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('/content/tajmahal.jpg',1)
cv2_imshow(a)
cv2.waitKey(0)

```
ii) #To write the image
```
colorImage = cv2.imread('/content/tajmahal.jpg',1)
cv2.imwrite('written.jpg',colorImage)
writtenImage = cv2.imread('written.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)


```
iii) #Find the shape of the Image
```python3
colorImage = cv2.imread('/content/tajmahal.jpg',1)
print(colorImage.shape)


```
iv) #To access rows and columns

```python3
import random
colorImage = cv2.imread('/content/tajmahal.jpg',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)


```
v) #To cut and paste portion of image
```python3
color_img = cv2.imread('/content/tajmahal.jpg',1)
tag = color_img[200:400,300:500]
color_img[200:400,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)


```

## Output:

### i) Read and display the image

![image](https://user-images.githubusercontent.com/94828517/225369765-776be545-8dfd-4bc3-8956-594eb82e1fa4.png)


### ii)Write the image


![image](https://user-images.githubusercontent.com/94828517/225369882-f5504db1-db74-4ddb-8764-c686b158a744.png)


### iii)Shape of the Image

<img width="344" alt="image" src="https://user-images.githubusercontent.com/94828517/225370008-3e724be5-8ee1-4dbe-8eee-4229a6b6a2aa.png">

### iv)Access rows and columns
![image](https://user-images.githubusercontent.com/94828517/225370066-3d31a104-edad-4a70-9a7f-ffb412a3a009.png)

### v)Cut and paste portion of image
![image](https://user-images.githubusercontent.com/94828517/225370128-f7adf07c-c5e2-4532-acc3-1588646efe4c.png)


## Result:
Thus the images are read, displayed, and written successfully using the python program.


