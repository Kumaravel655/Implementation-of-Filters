# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.
</br>
</br> 

### Step2
For performing smoothing operation on a image.

* Average filter
```
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
* Weighted average filter
```
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```

* Gaussian Blur
```
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```

* Median filter
```
median_blur=cv2.medianBlur(image,11)
```
</br>
</br> 

### Step3
For performing sharpening on a image.

* Laplacian Kernel
```
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```

* Laplacian Operator
```
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```
</br>
</br> 

### Step4
Display all the images with their respective filters.
</br>
</br> 



## Program:
### Developed By   :Kumaravel V
### Register Number:212220230027
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()



```
ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()




```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()



```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()



```
ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()




```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![Screenshot (88)](https://user-images.githubusercontent.com/75235334/166420627-31b2f484-5a06-488a-916d-a9829b2e6e64.png)


ii) Using Weighted Averaging Filter
![Screenshot (89)](https://user-images.githubusercontent.com/75235334/166420731-9e61152f-f8ae-4264-84ee-00b5fc102a07.png)

iii) Using Gaussian Filter

![Screenshot (90)](https://user-images.githubusercontent.com/75235334/166420809-96ee3135-cf27-439c-bc61-1f70323e9104.png)
iv) Using Median Filter
![Screenshot (91)](https://user-images.githubusercontent.com/75235334/166420887-77f63e8a-07c4-4ea3-af1c-0d2a7dfb2d11.png)
### 2. Sharpening Filters
 

i) Using Laplacian Kernal
![Screenshot (92)](https://user-images.githubusercontent.com/75235334/166420999-c01a439c-f41f-43aa-87d1-876f4c2c9c5e.png)
ii) Using Laplacian Operator
![Screenshot (93)](https://user-images.githubusercontent.com/75235334/166421063-230efd8a-1792-4488-be88-d05563a44d44.png)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
