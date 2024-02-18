#  Constrained Delaunay Triangulation 

##  1. Overview 

 ![avatar]( ff771924e659474e8a8d59d49d3ee1cb.png) 

   delaunayTriangulation class allows constraints on boundaries in a two-dimensional triangulation. This means that a pair of points in a triangulation can be selected and the edges used to connect those points can be constrained. This can be used as "applying pressure" to draw a boundary between a pair or pairs of points. The following example illustrates the effect of edge constraints on triangulation. The triangulation below is a Delaunay triangulation because it conforms to the empty circumcircle rule.  

##  2. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545464
  ```  
##  3. Display of results 

 ![avatar]( 139024e1b9a54bb699572667950a5036.png) 

    Constraints between vertices (V1, V3) have been followed, but the Delaunay rule is invalidated. In addition, the nearest neighbor relationship inherent in Delaunay triangulation is invalidated. This means that if the triangulation contains constraints, the nearestNeighbor search method provided by delaunayTriangulation cannot be supported. 

#  Triangulation of non-convex polygons 

##  1. Overview 

   In a typical application, a triangulation may consist of a large number of points, and there may be relatively few constrained sides in a triangulation. Such triangulation is considered a locally non-Delaunay triangulation, because many triangles in a triangulation may follow the Delaunay rule, but there may be some locally non-compliant triangles. In many applications, local relaxation of the empty circumscribed circle property is not a problem. Constrained triangulation is often used to triangulate non-convex polygons. These constraints establish a correspondence between the polygon side and the triangulated side. Using this relationship, a triangulation representing that region can be extracted. The following example illustrates how to triangulate a non-convex polygon using a constrained delaunayTriangulation. 

##  2. Code example 

 Define and draw polygons 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545464
  ```  
 ![avatar]( 382840ec64904681aebb9a437abb5e81.png) 

  Create and draw triangulations and polygon boundaries 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545464
  ```  
 ![avatar]( ea3cbfe09857449dacb7a27eb3d748fe.png) 

    This triangulation cannot be used to represent a polygon domain because some triangles straddle boundaries. You need to impose constraints on the edges that are cut by the triangulated edges. Since the requirements for all edges must be met, all edges need to be constrained. The following steps explain how to constrain all edges. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545464
  ```  
 ![avatar]( 7cac0530aa3f4ed5a803844ece3ad9d3.png) 

    The drawing shows that the triangulated sides meet the polygon boundary requirement. But the triangulation fills the recess. A triangulation representing the polygon domain is required in this case. You can extract the triangle from within the polygon using the delaunayTriangulation method isInterior. This method returns a logical array with true and false values indicating whether the triangle is within the bounded geometric domain. The analysis is based on the approximate curve theorem and the boundary is defined by the edge constraint. If the i-th logical flag is true, the i-th triangle in the triangulation is considered to be within the domain, otherwise it is considered to be outside the domain. Now use the isInterior method to calculate and plot a series of triangles in the domain. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545464
  ```  
 ![avatar]( fb5cf0029ff3443ab47d049a36b82ad7.png) 

    Save the pruning result. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545464
  ```  
