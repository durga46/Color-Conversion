# EX.NO :03

# <p align="center">  Color Conversion</p>
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

</br>
</br>
</br>


## Program:
```python
# Developed By:DurgaDevi P
# Register Number:212220230015
# i) Convert BGR and RGB to HSV and GRAY
import cv2
bfly_color_image = cv2.imread('butterfly.jpg')
cv2.imshow('original image',bfly_color_image)
hsv_image = cv2.cvtColor(bfly_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(bfly_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
gray_image = cv2.cvtColor(bfly_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(bfly_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)
hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV2BGR", hsv_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
cv2.imshow("BGR_COLOR ", img1)
img_ycrcb = cv2.cvtColor(img1 , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCRCB ", img_ycrcb)
img_bgr = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
cv2.imshow("RGB COLOR", img_bgr)
img_bgr_y = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
cv2
b,g,r = cv2.split(img1)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)
merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)
merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Output:
### i) BGR and RGB to HSV and GRAY
![162785803-3e644961-bed8-41c1-87da-775a5269b94a](https://github.com/durga46/Color-Conversion/assets/75235704/1d41ad99-cb97-4eaa-a50a-ebbae57bf799)


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
### ii) HSV to RGB and BGR

![162786267-2f866d43-97d6-4ede-af4a-7630d896ca3c](https://github.com/durga46/Color-Conversion/assets/75235704/83a2fccf-f538-4c43-97cf-7d758fdcbf28)


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### iii) RGB and BGR to YCrCb
![162785899-31ba113f-b84e-4827-941b-9d6ce449341f](https://github.com/durga46/Color-Conversion/assets/75235704/6237e028-0d77-44c8-b5fd-26ed00d77279)


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### iv) Split and merge RGB Image
![162785920-0adeb6be-37fb-4fa2-894d-8d37bcf57cca](https://github.com/durga46/Color-Conversion/assets/75235704/e214f369-4a55-4199-943c-c1c55a6e154b)



<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### v) Split and merge HSV Image
![162785930-8afcbaa8-b40d-476e-a245-a49ed439e685](https://github.com/durga46/Color-Conversion/assets/75235704/459aa076-dcc3-47e4-8332-c8098817ea92)


<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
