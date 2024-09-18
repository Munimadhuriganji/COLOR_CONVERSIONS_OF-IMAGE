### Developed By: GANJI MUNI MADHURI
### Register Number: 212223230060

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
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:

<table>
  <tr>
    <td width=50%>

### 1) Read and display the image
```Python
    import cv2
    image=cv2.imread('photo.jpg')
     cv2.imshow('Image Window',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-09-18 135052](https://github.com/user-attachments/assets/88f5c02c-5d3e-4d28-9c92-1fd3428d903a)

  </td>
  </tr>

   <tr>
    <td width=50%>

### 2)Draw Shapes and Add Text:
# i)Draw a line from the top-left to the bottom-right of the image.
```Python
  
import cv2
img = cv2.imread("lokesh.JPG")
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-09-18 135235](https://github.com/user-attachments/assets/3205840b-58f6-4a12-88b1-12158873eaca)




  </td>
  </tr>
  <tr>
    <td width=50%>

### ii)Draw Shapes and Add Text
```Python
   
import cv2
image = cv2.imread("lokesh.jpg")
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 150, (255,0, 0), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-09-18 135308](https://github.com/user-attachments/assets/08fdd345-990a-4538-b90b-22ab0af4c3a6)




  </td>
  </tr>
  <tr>
    <td>
      
### iii)Draw a rectangle around a specific region of interest in the image.
```Python
    
import cv2
image = cv2.imread("lokesh.JPG")
start=(0,0)
stop=(689,389)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(image,start,stop,color,thickness)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:
![Screenshot 2024-09-18 135344](https://github.com/user-attachments/assets/47cb6246-0a06-4e47-93eb-9801eac6ec66)



  </td>
  </tr>
  <tr>
    <td width=50%>
      
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
    
import cv2
img = cv2.imread("lokesh.JPG")
text = "OPENCV DRAWING"
position = (50, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
  </td>
  <td>
    
### OUTPUT:
![Screenshot 2024-09-18 135416](https://github.com/user-attachments/assets/5e6aadd5-4571-4a84-8e2c-ac70069a2ca1)




  </td>
  </tr>
</table>

### 3)Image Color Conversion
```Python

import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### OUTPUT:
![Screenshot 2024-09-18 135510](https://github.com/user-attachments/assets/b28bbbc3-55f0-4ec8-b15e-6d87063f3976)





### ii)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-09-18 135537](https://github.com/user-attachments/assets/4ba374cc-32cf-49fc-ac0f-a74f6ae1d506)





### iii) Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### OUTPUT:
![Screenshot 2024-09-18 135601](https://github.com/user-attachments/assets/8aa8431e-37c4-4694-b2ab-29d11adabd25)



### iv) Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-09-18 135627](https://github.com/user-attachments/assets/872b4f27-049c-4a8c-a6de-1c90d79d31e0)





### 4. Access and Manipulate Image Pixels:
```Python

import cv2
img = cv2.imread('lokesh.jpg', 1)
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255] 
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### OUTPUT:
![Screenshot 2024-09-18 135659](https://github.com/user-attachments/assets/9557dcaf-cbf2-447d-9b77-1ef635614481)
![Screenshot 2024-09-18 135925](https://github.com/user-attachments/assets/9cfca917-b938-4460-bf96-82fe8e1fc808)


### 5. Image Resizing:
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-09-18 135729](https://github.com/user-attachments/assets/2c049ccc-41b0-44e2-b1f8-098a330c72d2)

### 6.Image Cropping:
```

import cv2
image1=cv2.imread('lokesh.jpg',1)
x, y = 50, 50
width, height = 100, 100
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# OUTPUT:
![Screenshot 2024-09-18 135802](https://github.com/user-attachments/assets/fad57b1f-687e-4584-8bab-5c349c8f908b)

## 7.Image Flipping:
# i)Flip the original image horizontally and display it.
```

import cv2
img = cv2.imread("lokesh.JPG")
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# OUTPUT:
![Screenshot 2024-09-18 135828](https://github.com/user-attachments/assets/3c222013-91e0-4e5b-afad-5e5968271e97)

## ii.)Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("lokesh.JPG")
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# OUTPUT:
![Screenshot 2024-09-18 135852](https://github.com/user-attachments/assets/c43b370e-91ac-4b03-8c02-b03f1e7ec355)

## 8. Write and Save the Modified Image:
```
import cv2
img = cv2.imread("lokesh.JPG")
cv2.imwrite('lokesh1.jpg',img)
```
# OUTPUT:
![Screenshot 2024-09-18 135915](https://github.com/user-attachments/assets/78245ef2-68f2-4bee-b475-80873b4309d8)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







