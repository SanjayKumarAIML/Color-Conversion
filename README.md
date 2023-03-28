# Color Conversion
## AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.
<br>

### Step2:
Read the saved image using cv2.imread("filename.jpg").
<br>

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
<br>

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])
<br>

### Step5:
Output the image using cv2.imshow("OUTPUT", image)


<br>

## Program:

### Developed By:Sanjay Kumar S S
### Register Number:212221240048

### i) Convert BGR and RGB to HSV and GRAY:
```
img = cv2.imread('levi.jpg')
cv2.imshow('original',img)

bgr2hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR To HSV',bgr2hsv)

bgr2gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR To GRAY',bgr2gray)
rgb = cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rgb2hsv = cv2.cvtColor(rgb,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',rgb2hsv)

rgb2gray = cv2.cvtColor(rgb,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',rgb2gray)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### ii)Convert HSV to RGB and BGR:
```
cv2.imshow('HSV',bgr2hsv)

hsv2rgb = cv2.cvtColor(bgr2hsv,cv2.COLOR_HSV2RGB)
cv2.imshow('HSVtoRGB',hsv2rgb)

hsv2bgr = cv2.cvtColor(bgr2hsv,cv2.COLOR_HSV2BGR)
cv2.imshow('HSVtoBGR',hsv2bgr)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### iii)Convert RGB and BGR to YCrCb:
```
hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('HSV',hsv)
cv2.imwrite('2_HSV_Image.png',hsv)

hsv2bgr = cv2.cvtColor(hsv,cv2.COLOR_HSV2BGR)
cv2.imshow('HSVtoBGR',hsv2bgr)
cv2.imwrite('2_HSVtoBGR.png',hsv2bgr)

hsv2rgb = cv2.cvtColor(hsv,cv2.COLOR_HSV2RGB)
cv2.imshow('HSVtoRGB',hsv2rgb)
cv2.imwrite('2_HSVtoRGB.png',hsv2rgb)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### iv)Split and Merge RGB Image:
```
b,g,r = cv2.split(img)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)

merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### v) Split and merge HSV Image:
```
cv2.imshow("INITIAL_HSV ", bgr2hsv)

h,s,v = cv2.split(bgr2hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)

merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY:
<br>

![out1](https://user-images.githubusercontent.com/93427246/228268529-51cea3e4-3b8d-4e45-8950-6b883c03606d.JPG)

</br>

### ii) HSV to RGB and BGR:
<br>
<img src='https://user-images.githubusercontent.com/93427246/228269138-36138305-4ad4-409f-8f4e-8e820dcfa1a5.JPG'>
</img>

<br>

### iii) RGB and BGR to YCrCb:
<br>

![out3](https://user-images.githubusercontent.com/93427246/228270430-c6165f90-3dfd-4acc-aeaf-9014da8f5f36.JPG)

<br>

### iv) Split and merge RGB Image:
<br>
<img src='https://user-images.githubusercontent.com/93427246/228270443-2dd44685-2dee-4fe0-80a1-8e8e9bdbb662.JPG'>
</img>


<br>

### v) Split and merge HSV Image:
<br>

![out5](https://user-images.githubusercontent.com/93427246/228270475-3a61a878-d482-42a7-884f-466d6881302d.JPG)

<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
