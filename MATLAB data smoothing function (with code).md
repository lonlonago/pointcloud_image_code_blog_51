#  Function overview 

   Smooth the input data. 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   Smooth the response data in column vector y using a moving average filter. The calculation formula is:  

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   Smoothes data using a specified number of points or a specified scale of points. span is the number of data points used to calculate the smoothed value, specified as an integer or scalar value, and the range (0, 1) represents a small fraction of the total number of data points. If using the moving average method or the Savitzky-Golay method, the number of data points used to calculate the smoothed value must be odd. If span is specified as an even number or a fraction that results in an even number of data points, the span is automatically reduced by 1. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   Smoothes the data using the specified smoothing method. The smoothing method is as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   The Savitzky-Golay method uses the polynomial degree specified by the degree. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   The number of data points specified in the span calculation using Savitzky-Golay. The span must be odd and the degree must be less than the span. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   Specifies the value of the argument x. You can use this syntax with any of the arguments in the previous syntax. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   Perform operations on the GPU using gpuArray data. You can use gpuArray to respond to data in all previous syntax. This syntax requires ™ parallel computing toolbox. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
   Perform operations on the GPU using gpuArray input data. This syntax requires a parallel computing toolbox. 

#  Code example 

##  1. Smooth data using a moving average filter 

   Use a moving average filter and plot and compare the results. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
 ![avatar]( 413e57737db54be79e082043622ed263.png) 

 result display  

##  2. Use loess and rloess to smooth data 

   Create noisy data with two outliers, plot and compare the smoothed results with the loess and rloess methods. Then determine which method is less sensitive to outliers. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574530267
  ```  
 ![avatar]( 8763b6c4918c498e9642c574654eeaee.png) 

 result display  

#  III. Reference link 

 Smooth response data 

