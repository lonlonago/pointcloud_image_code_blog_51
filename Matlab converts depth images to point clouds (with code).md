#  Function overview 

##  1. Algorithm overview 

   The depth camera can obtain the distance information from the object to the camera, and can calculate the 3D camera coordinates of the pixel according to the distance information to generate a point cloud. The calculation formula is: in the formula, it is the depth value, the unit is meters; it is the scaling multiple of the depth value; it is the pixel coordinate, which is the 3D point cloud coordinate corresponding to the pixel; it is the focal length of the camera, which is the optical center of the camera, which is the so-called internal reference. The pose of the camera is also called the external parameter of the camera, which will change with the camera movement. Knowing the internal parameter can convert the depth image into a point cloud, and knowing the external parameter can splice the point clouds generated by the depth maps measured at different positions of the same object into a complete point cloud of ground objects. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596339
  ```  
   Convert a depth image to a point cloud using a camera internal function. The output point cloud is specified in 3D world coordinates, with its origin centered on the camera. The depth scale factor, usually provided by RGB-D camera manufacturers, specifies the segmentation factor for the depth image. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596339
  ```  
 Specify options using one or more name-value arguments and any combination of arguments from previous syntaxes. For example, pcfromdepth (depthImage, depthScaleFactor, intrinsics, DepthRange = [0, Inf]) sets the depth range to 2 element vector values [0, Inf]. 

 input parameter 

 Name-value corresponding parameter 

 output parameter 

##  3. References 

>  [1] The TUM data set is provided by J. Sturm, N. Engelhard, F. Endres, W. Burgard and D. Cremers under the CC-BY-4.0 license license. All warranties and representations are disclaimed; see the license for details. MathWorks® modified the name of the RGB-D SLAM Dataset and Benchmark dataset to use in the example. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596339
  ```  
#  III. Display of results 

##  1. Depth image 

 ![avatar]( 48c140dc398842d3ae32b79385aa1c5c.png) 

##  2. Color images 

 ![avatar]( 9049f83b01174ee395b147be94dd509a.png) 

##  3. Generate point clouds 

 ![avatar]( cfafbe227284405fa70bfce2509a3388.png) 

#  IV. Reference link 

 Matlab Point Cloud Toolbox - pcfromdepth 
