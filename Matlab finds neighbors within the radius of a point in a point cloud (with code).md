#  Function overview 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574562512
  ```  
   Returns the index of neighboring points within the radius of the query point in the input point cloud. The point cloud can be either an unordered point cloud or an ordered point cloud. The neighbors within the radius of the query point are calculated by using a Kd tree-based search algorithm. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574562512
  ```  
 Returns adjacent points within the radius of the query point in the input point cloud. The input point cloud is an ordered point cloud generated by the depth camera. The K-nearest neighbor of the query point is determined using the fast approximation K-nearest neighbor search algorithm. This function uses the camera projection matrix camMatrix to understand the relationship between adjacent points, thus speeding up the nearest neighbor search. However, the results have lower accuracy compared to the Kd tree-based method. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574562512
  ```  
 In addition to the input parameters in the above syntax, one or more name-value options are specified for the parameters. 

 input parameter 

 Name-value corresponding parameter 

   Specify the optional parameter pair as Name1 = Value1,..., NameN = ValueN, where Name is the parameter name and Value is the corresponding value. The name-value argument must appear after the other arguments, but the order of the argument pairs does not matter. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574562512
  ```  
 output parameter 

##  2. References 

>  [1] Muja, M. and David G. Lowe. “Fast Approximate Nearest Neighbors with Automatic Algorithm Configuration”. In VISAPP International Conference on Computer Vision Theory and Applications. 2009. pp. 331–340. 

#  Disordered point cloud 

##  1. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574562512
  ```  
##  2. Results display 

 ![avatar]( 01d0270162b341dfbbf0863ba43ab747.png) 

#  III. Orderly point cloud 

##  1. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574562512
  ```  
##  2. Results display 

 ![avatar]( 16939efceeb6499e901e3c107cae3f10.png) 

#  IV. Reference link 

 Matlab Point Cloud Toolbox - findNeighborsInRadius 

