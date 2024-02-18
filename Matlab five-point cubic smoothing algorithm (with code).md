#  First, the principle of the algorithm 

##  1. Principle analysis of five-point cubic smoothing algorithm 

   The five-point cubic smoothing algorithm belongs to a kind of smoothing filtering algorithm. In the smoothing filtering algorithm, the commonly used ones are: spline difference function smoothing method, average calculation smoothing method and five-point cubic smoothing method. The spline difference function smoothing method adopts the method of spline interpolation to approximate the sampling point to achieve smoothing. The algorithm is flexible and changeable, and the effect is good. However, the calculation process of this method is relatively complicated, and the performance of smoothing amplitude is poor. Although the average calculation smoothing method is relatively simple, the filtering effect is not good. The principle of the five-point cubic smoothing method to achieve smoothing filtering is to use the polynomial least squares method to approximate the sampling point. The algorithm is very simple and the filtering effect is also good. The principle of the five-point cubic smoothing algorithm: Let the experimental data on each isometric node be Set the equidistance between the two nodes as, do the exchange, then the original node is transformed into. The obtained experimental data is fitted with a sub-polynomial, and the fitting polynomial is: Wherein, the undetermined coefficient in equation (1) is determined using the least squares method, let: In order to minimize, it is derived separately and made equal to 0, and a system of equations can be obtained: This equation is called a normal system of equations. When = 2 (that is, 5 nodes), = 3, a normal system of equations will be obtained, which will be solved and carried into (3), and let, the five-point cubic smoothing formula can be obtained as follows: In the formula: the improved value of is. The algorithm requires the number of nodes to be at least 5. When the number of nodes exceeds 5, in order to calculate symmetrically, except for the two ends of the equation (4)~ formula (8), the rest are smoothed by formula (6), which is equivalent to using different cubic least squares polynomials for smoothing calculation on each sub-interval. After the above derivation, it can be concluded that in the case of equidistant nodes, only experimental data are used in the formula of the five-point cubic smoothing algorithm, and it has nothing to do with, and. The characteristics of the five-point cubic smoothing method preserve the characteristics of the original curve well, and at the same time effectively eliminate the existing interference components, which increases the readability compared with the original curve. 

##  2. References 

>  [1] YU Peng, Yan Liangwen, Yu Yue, Cao Cola, Huang Shan, Dong Xudong, Chen Jiale. Application of five-point cubic smoothing algorithm in PPG signal noise reduction [J]. Metrology and Testing Technology, 2020, 47 (06): 47-50 + 53. 

#  Code implementation 

 mean5_3.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529910
  ```  
 main.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574529910
  ```  
#  III. Display of results 

 ![avatar]( 7a95d87d316842d8b43736c37c8f2f86.png) 

