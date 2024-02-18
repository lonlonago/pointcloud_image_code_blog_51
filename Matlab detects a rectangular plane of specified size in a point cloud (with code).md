#  I. Overview 

##  1. Algorithm overview 

   detectRectangularPlanePoints: Detects a rectangular plane of specified size in the point cloud 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553806
  ```  
 Detects and extracts rectangular planes of specified size from the input point cloud ptCloudPlanes 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553806
  ```  
 Detects a rectangular plane from the input ptCloudArray. The function returns a logical vector ptCloudUsed that indicates the point cloud in which the rectangular plane was detected. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553806
  ```  
 Detects a rectangular plane from a set of point cloud files (ptCloudFileNames) and returns any combination of the output parameters of the previous syntax. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553806
  ```  
 Returns the index of the points within the rectangular plane detected in each point cloud, along with any previous parameter combinations. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553806
  ```  
 Specify options for parameters using one or more name-values. For example, 'RemoveGround', true Set the'RemoveGround 'flag to true, which removes the ground plane from the input point cloud before processing. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553806
  ```  
#  III. Display of results 

 ![avatar]( a2e8ab5140734e4aa5492a8d691f8e31.png) 

 The original point cloud, the plane detected from the point cloud, and the rectangular plane detected visually on the input point cloud 

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  V. Reference links 

 Matlab Point Cloud Toolbox - detectRectangularPlanePoints 

