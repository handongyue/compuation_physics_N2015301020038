# QUESTION 1

## The position of an object moving 

the position of an object moving horizontally with a constant velocity,v,is described by the equation
:<br/>  

<img src="http://latex.codecogs.com/gif.latex?\frac{dx}{dt}=v" alt="" title="" />  <br/>
Assuming that the velocity is a constant ,say v=40m/s, use the Euler method to solve this for x as a 
function of time. Compare your result with the exact solution.

## Analysis
采用for循环来达到这一个运算 以每一次的循环来输出当前的t值及对应的x值，并且用pylab绘制出x随t的变换的图像，设置
循环次数为1000次

## Code

```python
import numpy as np    
import pylab as pl 
Number_x=[]    
t=[]#建立数组   
dt=0.01#定义dt
t.append(0)    
for i in range(1000):    
    Nx=(40)*t   
    tadd=t[i]+dt    
    Number_x.append(Nx)    
    t.append(tadd)#定义循环
t_max=t[10]    
pl.plot(t,Number_x,'x')    #绘制图像
pl.title('The position of an object moving ')    
pl.xlabel('the time')    
pl.ylabel('The displacement')    
pl.show()
```
##Result




