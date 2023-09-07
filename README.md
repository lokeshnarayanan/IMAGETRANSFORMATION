# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Write a code to translation of the image.

### Step3:
Write a code for scaling of the image.

### Step4:
Write a code for shearing of the image.

### Step5:
Write a code for reflection of the image.

### Step6:
Write a code to rotation of the image.

### Step7:
Write a code to cropping of the image.

### Step8:
Display all the Transformed images.

## Program:
```python
Developed By:Lokesh N
Register Number:212222100023
```

i)Image Translation
```python
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv

```
```


image = cv.imread("moon.png")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)

plt.axis("off")
plt.imshow(image)
plt.show()

rows,cols,dim = image.shape

M = np.float32([[1,0,100], [0,1,50],[0,0,1]])
translated_image= cv.warpPerspective(image, M, (cols, rows))

plt.axis("off")
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling

```
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()
```

iii)Image shearing

```
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()
```

iv)Image Reflection

```
M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(ref_imagex)
plt.show()

plt.axis("off")
plt.imshow(ref_imagey)
plt.show()
```


v)Image Rotation

```
angle=np.radians(10)

matrix=np.float32([[np.cos(angle),-np.sin(angle),0],
                                [np.sin(angle),np.cos(angle),0],
                                [0,0,1]])

Rotated_image=cv.warpPerspective(image,matrix,(cols,rows))

plt.axis("off")
plt.imshow(Rotated_image)
```


vi)Image Cropping

```
crop_img = image[150:600 ,350:900]

plt.axis("off")
plt.imshow(crop_img)
plt.show()

```
## Output:
### i)Image Translation
![Screenshot from 2023-09-07 10-38-51](https://github.com/lokeshnarayanan/IMAGETRANSFORMATION/assets/119393019/93ea03b5-4660-4075-9d0d-3cac9ec49736)

### ii) Image Scaling
![Screenshot from 2023-09-07 10-39-14](https://github.com/lokeshnarayanan/IMAGETRANSFORMATION/assets/119393019/1df18752-29ba-414b-8f6d-11f754b905d4)

### iii)Image shearing
![Screenshot from 2023-09-07 10-39-43](https://github.com/lokeshnarayanan/IMAGETRANSFORMATION/assets/119393019/feae4a26-7ba6-4dfb-b11b-ee82979dce8f)

### iv)Image Reflection
![Screenshot from 2023-09-07 10-40-01](https://github.com/lokeshnarayanan/IMAGETRANSFORMATION/assets/119393019/a552f796-1bd2-4354-9336-f7877f51a6e6)

### v)Image Rotation
![Screenshot from 2023-09-07 10-40-15](https://github.com/lokeshnarayanan/IMAGETRANSFORMATION/assets/119393019/32a0b7e9-8ec0-4784-aef7-cb61df6bbdbf)

### vi)Image Cropping
![Screenshot from 2023-09-07 10-40-26](https://github.com/lokeshnarayanan/IMAGETRANSFORMATION/assets/119393019/6dafcd62-d13c-4112-91ea-4f6f0ee7959e)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
