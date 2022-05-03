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
![Screenshot (82)](https://user-images.githubusercontent.com/75235334/166419270-9df95d38-0cd6-4597-be69-c6605beded15.png)


ii) Using Weighted Averaging Filter
![Screenshot (83)](https://user-images.githubusercontent.com/75235334/166419347-4fe9aad3-dc61-40fe-aa06-ed2ed80e5d79.png)

iii) Using Gaussian Filter

![Screenshot (84)](https://user-images.githubusercontent.com/75235334/166419707-d8852f23-40a7-45a0-b256-61d0b64a0262.png)

iv) Using Median Filter
![Screenshot (85)](https://user-images.githubusercontent.com/75235334/166419805-39d3bc46-cb10-4467-9b63-d450a3595dba.png)

### 2. Sharpening Filters
 

i) Using Laplacian Kernal
![Screenshot (86)](https://user-images.githubusercontent.com/75235334/166419963-c5dc8888-7882-4479-8f13-02190cf75234.png)

ii) Using Laplacian Operator
![Screenshot (87)](https://user-images.githubusercontent.com/75235334/166420065-fcc49e28-804a-47d8-a9a9-0f9a214a2d96.png)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
