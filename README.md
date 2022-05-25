Steppingage-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))

### Step3:
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

### Step4:
Shear the image using
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

### Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))

### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

### Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

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
![raw](https://user-images.githubusercontent.com/75243072/165880772-6ed7ab12-b9f2-4e5d-aa5e-d50b4ead6dd4.png)

### i)Image Translation
![it](https://user-images.githubusercontent.com/75243072/165880837-b6120835-d5b2-4dc8-b8a3-52d1ca004d85.png)

### ii) Image Scaling
![is](https://user-images.githubusercontent.com/75243072/165880859-ca927e6f-3af9-4985-a7e6-d874b1b656df.png)

### iii)Image shearing
![ish](https://user-images.githubusercontent.com/75243072/165880871-63a3e350-add8-4536-89f4-ff92ec8c625d.png)

### iv)Image Reflection
![ir](https://user-images.githubusercontent.com/75243072/165880889-b31e342f-7221-4bd6-8da6-e4c04bd2975a.png)

### v)Image Rotation
![irot](https://user-images.githubusercontent.com/75243072/165880918-a19da6a3-857b-459a-8c07-21519ae51ce5.png)

### vi)Image Cropping
![ic](https://user-images.githubusercontent.com/75243072/165880942-471f4b62-ffcd-47a2-950e-ec9030d60c98.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
