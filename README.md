# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image
```
import cv2
image=cv2.imread('naturek.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('NATUREK',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-02 091158](https://github.com/user-attachments/assets/520ea58c-0186-456d-9b9e-9e23c56bfb46)

### ii)Write the image
```
cv2.imwrite('n.jpg',image)
```
![Screenshot 2024-09-02 091254](https://github.com/user-attachments/assets/697995d1-a746-4269-b46d-586703baa750)

### iii)Shape of the Image
```
print(image.shape)
```
![Screenshot 2024-09-02 091336](https://github.com/user-attachments/assets/df5eb1bd-9d06-451f-9a3a-e18bf47efa91)

### iv)Access rows and columns
```
import random
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)]
cv2.imshow('nature',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-02 091556](https://github.com/user-attachments/assets/e875190d-c634-48cf-aa20-a4c878a7c96a)

### v)Cut and paste portion of image
```
image=cv2.imread('naturek.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('nature',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-02 092017](https://github.com/user-attachments/assets/55068bdc-635a-4103-a148-a7dd8b90a06a)

### vi) BGR and RGB to HSV and GRAY
```
img = cv2.imread('naturek.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![1 1e](https://github.com/user-attachments/assets/797d56e2-2f47-41a5-9f11-acbf75964e7c)

### vii) HSV to RGB and BGR
```
img = cv2.imread('naturek.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![1 2e](https://github.com/user-attachments/assets/a84fd9f6-f8eb-49e7-8f46-5499de62eaa2)

### viii) RGB and BGR to YCrCb
```
img = cv2.imread('naturek.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### ix) Split and merge RGB Image
```
img = cv2.imread('naturek.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![1 4e](https://github.com/user-attachments/assets/c93be34a-c993-45f6-85f7-4e273b2b85f4)

### x) Split and merge HSV Image
```
img = cv2.imread("naturek.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![1 5e](https://github.com/user-attachments/assets/dfe61346-8857-4373-acfa-16eb1c9dbd7f)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







