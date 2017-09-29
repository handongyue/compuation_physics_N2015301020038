# QUESTION 1

## The position of an object moving 

the position of an object moving horizontally with a constant velocity,v,is described by the equation
:<br/>  

<img src="http://latex.codecogs.com/gif.latex?\frac{dx}{dt}=v" alt="" title="" />  <br/>
Assuming that the velocity is a constant ,say v=40m/s, use the Euler method to solve this for x as a 
function of time. Compare your result with the exact solution.

## Analysis
采用for循环来达到这一个运算 以每一次的循环来输出当前的t值及对应的x值，并且用pylab绘制出x随t的变换的图像，设置
循环次数为100次

## Code

```python
import numpy as np    
import pylab as pl 
Number_x=[]    
t=[]#建立数组
print('The initial position')   
number_a=float(input())
Number_x.append(number_a)  
print('the time step') 
dt=float(input())#定义初始时刻原子数和步长
t.append(0)    
for i in range(1000):    
    NA=Number_x[i]+(40)*dt    
    tadd=t[i]+dt    
    Number_x.append(NA)    
    t.append(tadd)#定义循环
t_max=t[-1]    
pl.plot(t,Number_x,'x')    #绘制图像
pl.title('The position of an object moving ')    
pl.xlabel('the time')    
pl.ylabel('The displacement')    
pl.show()
```
##Result




