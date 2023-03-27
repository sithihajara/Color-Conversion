# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.

### Step2:
Read the saved image using cv2.imread("filename.jpg").

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])

### Step5:
Output the image using cv2.imshow("OUTPUT", image)

## Program:

### Developed By:Sithi Hajara I
### Register Number:212221230102

## i) Convert BGR and RGB to HSV and GRAY
```
import cv2
car_image=cv2.imread('clr.png')
cv2.imshow('clr',clr_image)

#BGR2HSV
hsv_image=cv2.cvtColor(clr_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)

#RGB2HSV
hsv_image1=cv2.cvtColor(clr_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)

#BGR2GRAY
gray_image=cv2.cvtColor(clr_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
#RGB2GRAY
gray_image1=cv2.cvtColor(clr_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## ii)Convert HSV to RGB and BGR
```
import cv2
hsv_image=cv2.imread('clr.png')
cv2.imshow('Original hsv image',hsv_image)

#HSV2RGB
rgb_image=cv2.cvtColor(hsv_image,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV 2 RGB',rgb_image)

#HSV2BGR
bgr_image=cv2.cvtColor(hsv_image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV 2 BGR',bgr_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## iii)Convert RGB and BGR to YCrCb
```
import cv2
lam_image=cv2.imread('clr.png')
cv2.imshow('original image',lam_image)

#RGB2YCrCb
ycrcb_image=cv2.cvtColor(lam_image,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB 2 YCrCb',ycrcb_image)

#BGR2YCrCb
ycrcb_image1=cv2.cvtColor(lam_image,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR 2 YCrCb',ycrcb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## iv)Split and Merge RGB Image
```
import cv2
l_image=cv2.imread('clr.png')
blue= l_image[:,:,0]
green= l_image[:,:,1]
red= l_image[:,:,2]
cv2.imshow('blue_image',blue)
cv2.imshow('green_image',green)
cv2.imshow('red_image',red)
merge_image=cv2.merge((blue,green,red))
cv2.imshow('merge',merge_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## v) Split and merge HSV Image
```

import cv2
l_image=cv2.imread('clr.png')
hsv_image=cv2.cvtColor(l_image,cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv_image)
cv2.imshow('H',h)
cv2.imshow('S',s)
cv2.imshow('V',v)
merge=cv2.merge((h,s,v))
cv2.imshow('MERGE',merge)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY
![bg1](https://user-images.githubusercontent.com/94219582/228022882-e4523440-2366-4685-96f9-4310b071bade.png)
![BG](https://user-images.githubusercontent.com/94219582/228023938-ac9aac2c-9d3e-4c7c-b13a-5df0f063ce36.png)

### ii) HSV to RGB and BGR
![HSV](https://user-images.githubusercontent.com/94219582/228024845-13f5129a-6ca2-449a-8120-b11d7aacfd67.png)

### iii) RGB and BGR to YCrCb
![RGB](https://user-images.githubusercontent.com/94219582/228025454-768c9b7e-f224-489f-83e6-b3d69836d0e8.png)

### iv) Split and merge RGB Image
![split](https://user-images.githubusercontent.com/94219582/228026155-58b58bec-6a4d-4b76-933d-3ca95a6f87b1.png)

### v) Split and merge HSV Image
![mer](https://user-images.githubusercontent.com/94219582/228030031-55b467ae-31ed-419e-84c6-f4544d416b4c.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
