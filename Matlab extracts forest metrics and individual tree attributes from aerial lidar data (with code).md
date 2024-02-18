#  Function overview 

##  1. Algorithm overview 

 ![avatar]( 7ccfc8c7b03b4b5eb6308fa44782fa58.png) 

   This example shows how forest metrics and attributes of individual trees can be extracted from aerial LiDAR data. Forest research and applications are increasingly making use of LiDAR data obtained from airborne laser scanning systems. Point cloud data from high-density LiDAR can measure not only forest metrics, but also attributes of individual trees. This example uses point cloud data from an LAZ file captured by an airborne LiDAR system as input. In this example, forest metrics are first extracted by classifying point cloud data into ground points and vegetation points, and then individual tree attributes are extracted by splitting vegetation points into individual trees. The following figure outlines the process.  

##  2. Load and visualize data 

   Unzip the forestData.zip to a temporary directory and load the point cloud data from the LAZ file forestData. laz, into the MATLAB ® workspace. The data comes from Open terrain Dataset [1]. The point cloud mainly contains ground points and vegetation points. Use the readPointCloud function of the lasFileReader object to load the point cloud data into the workspace. Use the pcshow function to visualize the point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
 ![avatar]( 3bbceeb43c5c4a0cbd17578615232513.png) 

##  3. Split and extract ground points and non-ground points 

   Ground segmentation is a preprocessing step that separates vegetation data to extract forest metrics. Use the segmentGroundSMRF function to segment the data loaded from the LAZ file into ground and non-ground points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
##  4. Elevation normalization 

   Use elevation normalization to eliminate the effect of terrain on vegetation data. Use points with normalized elevations as inputs to calculate forest metrics and tree attributes. The elevation normalization steps are as follows: 1. Use the groupsummary function to eliminate duplicate points on axes and axes, if any. 2. Use the scatteredInterpolant object to create an interpolation to estimate each ground point in the point cloud data. 3. Subtract the interpolated ground elevation from the original elevation to normalize the elevation of each point. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
 ![avatar]( 8e5ac3816d85458a883da9c7edef8bd3.png) 

##  5. Extract forest indicators 

   The forest metrics are extracted from the normalized points using the helperExtractForestMetrics helper function, which is attached to this example as a supporting file. The helper function first divides the point cloud into a grid based on the supplied gridSize and then calculates the forest metrics. The helper function assumes that all points with a normalized height below the cutoff height are ground and the rest are vegetation. Calculate these forest metrics: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
 ![avatar]( 5423d9c186844af5b6a795ea5c54fbcb.png) 

##  6. Canopy height model 

   The canopy height model (CHM) is a raster representation of the height of trees, buildings, and other structures above ground topography. Use CHM as input for tree detection and segmentation. Generate CHM from normalized elevation values using the pc2dem function. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
 ![avatar]( bdc5930288fc4483b7cad49a76641323.png) 

##  7. Detect the top of the tree 

   The tree top is detected using the helperDetectTreeTops helper function, which is attached to this example as a support file. The helper function detects the tree top by looking for a local maximum within a variable window size in CHM. For tree top detection, the helper function only considers points with a normalized height greater than minTreeHeight. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
 ![avatar]( 4849511b47e34b6db22ac05d5e27ea8f.png) 

##  8. Single tree segmentation 

   Use the helperSegmentTrees helper function, which is attached to this example as a support file, to split individual trees. The helper function utilizes a marker-controlled watershed segmentation to split individual trees. First, the function creates a binary marker image indicating the tree top position with a value of 1. Then, the function filters the CHM complement by a minimum value puzzle to remove the smallest value that is not the top of the tree. Finally, the function performs a watershed segmentation on the filtered CHM complement to split individual trees. After segmentation, the individual tree segments are visualized. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
##  9. Extract tree attributes 

   Individual tree properties are helperExtractTreeMetrics extracted using the helper function, which is attached to this example as a support file. First, the function identifies points belonging to individual trees from labels. The function then extracts tree properties such as the tree top position along axes and axes, the tree's approximate height, crown diameter, and area. The helper function returns properties as a table, where each row represents the properties of an individual tree. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
 ![avatar]( 5692d1d8dc964d11b4551b7224dc8aa9.png) 

#  II. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524848
  ```  
#  III. Display of results 

##  1. Input point cloud 

 ![avatar]( b915db9d8ef74a229dbdcbb8448e0d64.png) 

##  2. Output results 

 ![avatar]( cc4a71e34e93479f8695a9746f767764.png) 

#  IV. Reference link 

 matlab点云工具箱——Extract Forest Metrics and Individual Tree Attributes from Aerial Lidar Data 

#  V. References 

>  [1] Thompson, S. Illilouette Creek Basin Lidar Survey, Yosemite Valley, CA 2018. National Center for Airborne Laser Mapping (NCALM). Distributed by OpenTopography. https://doi.org/10.5069/G96M351N. Accessed: 2021-05-14 

>  [2] Ma, Qin, Yanjun Su, and Qinghua Guo. “Comparison of Canopy Cover Estimations From Airborne LiDAR, Aerial Imagery, and Satellite Imagery.” IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing 10, no. 9 (September 2017): 4225–36. https://doi.org/10.1109/JSTARS.2017.2711482. 

>  [3] Richardson, Jeffrey J., L. Monika Moskal, and Soo-Hyung Kim. “Modeling Approaches to Estimate Effective Leaf Area Index from Aerial Discrete-Return LIDAR.” Agricultural and Forest Meteorology 149, no. 6–7 (June 2009): 1152–60. https://doi.org/10.1016/j.agrformet.2009.02.007. 

>  [4] Pitkänen, J., M. Maltamo, J. Hyyppä, and X. Yu. “Adaptive Methods for Individual Tree Detection on Airborne Laser Based Canopy Height Model.” International Archives of Photogrammetry, Remote Sensing and Spatial Information Sciences 36, no. 8 (January 2004): 187–91. 

>  [5] Chen, Qi, Dennis Baldocchi, Peng Gong, and Maggi Kelly. “Isolating Individual Trees in a Savanna Woodland Using Small Footprint Lidar Data.” Photogrammetric Engineering & Remote Sensing 72, no. 8 (August 1, 2006): 923–32. https://doi.org/10.14358/PERS.72.8.923. 

