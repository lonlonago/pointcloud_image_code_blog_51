#  Function overview 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574527711
  ```  
 Returns the points in the region of interest (ROI) in the input point cloud. The points in the specified ROI are obtained using a KD tree-based search algorithm. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574527711
  ```  
   Returns the points within the ROI area of the input point cloud. The input point cloud is an organized point cloud generated by a depth camera. The points within the specified ROI are obtained by a fast approximate neighborhood search algorithm. This function utilizes the camera projection matrix cam matrix to understand the relationship between adjacent points, thus speeding up the search. However, the results have lower accuracy compared to the KD tree-based method. 

>  Attention:

This method only supports organized point cloud data generated by RGB-D sensors. estimateCameraMatrix can be used to estimate the camera projection matrix for a given point cloud data. 

##  2. References 

>  [1] Muja, M. and David G. Lowe. “Fast Approximate Nearest Neighbors with Automatic Algorithm Configuration”. In VISAPP International Conference on Computer Vision Theory and Applications. 2009. pp. 331–340. 

#  Code example 

##  1. Find the point in the cuboid ROI in the point cloud 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574527711
  ```  
##  2. Results display 

 ![avatar]( e3ac61efa4fb4f08b0d9177096c52539.png) 

##  3. Find the points in the cuboid ROI in an organized point cloud 

   Use camera projection matrix to find points in cuboid ROI in organized point cloud data. Calculate camera projection matrix from sampled point cloud data points and their corresponding image point coordinates. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574527711
  ```  
##  4. Display of results 

 ![avatar]( 5d8fc93a49514e10833073a1da4c263c.png) 

#  III. Reference link 

 Matlab Point Cloud Toolbox - findPointsInROI 
