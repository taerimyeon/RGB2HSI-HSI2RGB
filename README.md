# RGB2HSI-HSI2RGB
Implementation of Digital Image Processing color conversion from RGB to HSI color space, and vice versa. Plus histogram equalization technique on both color spaces.  
  
## The Libraries you will need
I wrote this in Jupyter notebook (Python), so you will need to install the following Python libraries:  
-  OpenCV
-  Matplotlib
-  NumPy
  
## RGB to HSI
The implementation of RGB to HSI color space conversion is as follows. Given the normalized value of R, G, and B in the range between 0 and 1, we can compute H, S, and I as:  
![RGB2HSIEqu](https://github.com/tttdddstvn/RGB2HSI-HSI2RGB/blob/master/Images/rgb2hsi.PNG)  
Where H in the range of 0-360, S is 0-1, and I is also 0-1. I decided to keep the value of H as it is (not following the range of 0-360) because matplotlib will rescale it automatically for display, but you can modify it yourself.  
  
## HSI to RGB
In this section, first I scale the H value to be in the range of 0-360. The implementation of HSI to RGB color space conversion is as follows:  
![HSI2RGBEqu](https://github.com/tttdddstvn/RGB2HSI-HSI2RGB/blob/master/Images/hsi2rgb.PNG)  
Note that after we obtain the temporary values of R, G, and B (denoted as r, g, and b in the equation) we still need to multiply them with 3 and intensity value I.  

## Histogram Equalization on RGB and HSI
