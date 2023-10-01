# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image

### Step5:
Find reflection of image. 

### Step 6:
Rotate the image.

### Step 7:
Crop the image

### Step 8:
Display all the Transformed images. 


## Program:
```
Developed By:ROSHINI R K
Register Number:212222230123
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
c_image = cv2.imread("dt4.jpg")
c_image = cv2.cvtColor(c_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(c_image)
plt.show()
rows,cols,dim = c_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

ii) Image Scaling
rows,cols,dim = c_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(c_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()


iii)Image shearing
rows,cols,dim = c_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection
rows,cols,dim = c_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(c_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(c_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation
rows,cols,dim = c_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(c_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
rows,cols,dim = c_image.shape
cropped_img=c_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```

## Output:
### Input Image:
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/49a228be-40d5-4177-b9f0-ddf0a66e3471)

### i)Image Translation
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/80786428-6b5f-434d-8b61-368584a49891)

### ii) Image Scaling
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/de8bd18d-9abc-483b-98c9-4c3a98e9e70a)



### iii)Image shearing
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/c06ed881-b905-4bbf-bbfb-5a6aef9a604b)
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/2d738d12-78d9-4c9b-b014-a97ab80d356a)



### iv)Image Reflection
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/a0db56ca-b1c7-4dea-bb50-36324e2a912b)
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/34577a31-f7f3-4f5e-8941-b6b00ece1957)




### v)Image Rotation
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/4905c9dc-ee52-4880-b224-5e1d2d197917)




### vi)Image Cropping
![image](https://github.com/roshiniRK/IMAGETRANSFORMATION/assets/118956165/d6497f1c-1408-4132-b292-c0402d471332)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
