# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.
### Step2:
Translate the image using Translation_matrix.
### Step3:
Scale the image using Scaling_Matrix.
### Step4:
Shear the image using Shearing_matrix.
### Step5:
Reflection of image can be achieved through the code Reflection_matrix_row.
### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix
### Step7:
Crop the image using cropped_image.
### Step8:
Display all the Transformed images.

## Program:

```python
Developed By:Kumaran.B
Register Number:212220230026
import cv2
import numpy as np
import matplotlib.pyplot as plt
img=cv2.imread("naturekumaran.jpeg")
img=cv2.resize(img,(500,400))
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
cv2.imshow("title",img)
cv2.waitKey(0)
cv2.destroyAllWindows()
rows,cols,dim=img.shape
i)Image Translation
M=np.float32([[1,0,50],
          [0,1,75],
          [0,0,1]])
translated_img=cv2.warpPerspective(img,M,(cols,rows))
cv2.imshow("title",translated_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
ii) Image Scaling
M=np.float32([[1.5,0,0],
          [0,1.8,0],
          [0,0,1]])
scaled_img=cv2.warpPerspective(img,M,(cols,rows))
cv2.imshow("title",scaled_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
iii)Image shearing
Mx=np.float32([[1,0.5,0],
          [0,1,75],
          [0,0,1]])
My=np.float32([[1,0,0],
              [0.5,1,0],
               [0,0,1]])
shx_img=cv2.warpPerspective(img,Mx,(int(cols),int(rows)))
shy_img=cv2.warpPerspective(img,My,(int(cols),int(rows)))
cv2.imshow("title1",shx_img)
cv2.imshow("title2",shy_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
iv)Image Reflection
Mx=np.float32([[1,0,0],
          [0,-1,rows],
          [0,0,1]])
My=np.float32([[-1,0,cols],
              [0,1,0],
               [0,0,1]])
refx_img=cv2.warpPerspective(img,Mx,(int(cols),int(rows)))
refy_img=cv2.warpPerspective(img,My,(int(cols),int(rows)))
cv2.imshow("title1",refx_img)
cv2.imshow("title2",refy_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
v)Image Rotation
angle=np.radians(27)
Rotation_matrix=np.float32([[np.cos(angle),-np.sin(angle),0],
                                [np.sin(angle),np.cos(angle),0],
                                [0,0,1]])
rotimg=cv2.warpPerspective(img,Rotation_matrix,(int(cols),int(rows)))
cv2.imshow("title1",rotimg)
cv2.waitKey(0)
cv2.destroyAllWindows()
vi)Image Cropping
cropimg=img[50:400,50:400]
cv2.imshow("title1",cropimg)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Normal image
![Screenshot (328)](https://user-images.githubusercontent.com/75243072/174750368-303a4238-d687-4370-a20d-3ab4d5efef3b.png)


### i)Image Translation
![Screenshot (331)](https://user-images.githubusercontent.com/75243072/174750567-95fd1dbf-ab8e-4827-b5b3-4eef43bb34b3.png)


###  ii)Image Scaling
![Screenshot (332)](https://user-images.githubusercontent.com/75243072/174751587-731217fb-4da4-42e8-bd02-3de65bc7637d.png)


### iii)Image shearing 
![Screenshot (333)](https://user-images.githubusercontent.com/75243072/174751704-4368cfdb-8058-4f96-993e-192880b645b3.png)



### iv)Image Reflection
![Screenshot (300)](https://user-images.githubusercontent.com/75243072/173769302-6056934f-a6f0-47ba-94a6-0723fddce6a7.png)

### <br><br>v)Image Rotation
![Screenshot (334)](https://user-images.githubusercontent.com/75243072/174752240-1f1e11e5-f7f3-432c-b644-036876b40cb8.png)


### <br><br><br><br><br><br><br><br>vi)Image Cropping
![Screenshot (335)](https://user-images.githubusercontent.com/75243072/174752305-e0bcab74-ce31-4592-a5f3-3ba5ca368206.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
