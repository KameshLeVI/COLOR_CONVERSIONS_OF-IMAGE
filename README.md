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

### Developed By: KAMESH D
### Register Number: 212222240043


## Output:

<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('KAMESH',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![dip 1](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/59f9f67d-1000-450a-811b-72bfd19bf755)

  </td>
  </tr>

   <tr>
    <td width=50%>


### ii)Write the image
```
    import cv2
    image=cv2.imread('dip.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:
![dip2](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/2bd6d280-c130-4c78-ab5c-c96596f24ae5)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('dip.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![dip3](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/84a5e5b0-3dbc-42df-aa2b-a786edd29809)


  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:
![dip4](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/6e99f070-9aae-469f-8b3c-5e2f378fb8d3)


  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```
   import cv2
   image=cv2.imread('dip.jpg',1)
   image=cv2.resize(image,(300,300))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('image1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![dip5](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/cbaff5a8-ca34-44be-ba27-261ab726efce)


  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('dip.jpg',1)
img = cv2.resize(img,(200,200))
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

### OUTPUT:
![dip6](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/d36f49bd-9008-4750-96ac-96c4b18d352b)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![dip7](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/1eba5c3a-3104-4230-9b89-a802c6c08e29)

 
### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![dip8 5](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/90418129-bca5-402b-a087-a8e1e73436b8)




### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('blue.jpg',1)
img = cv2.resize(img,(200,200))

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

### OUTPUT:


![dip8](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/665fc7b2-429a-46bd-a468-5988f73b8167)



### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("blue.jpg",1)
img = cv2.resize(img,(200,200))
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

### OUTPUT:

![dip9](https://github.com/KameshLeVI/COLOR_CONVERSIONS_OF-IMAGE/assets/120780633/1a829fa5-9601-4b63-92c8-fd334241379e)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







