# 使用python求解

##  一·高等数学求解

### 1.$\sqrt{x}^\frac{1}{\sqrt(x)-1}$当x$\to$1时的极限. 

启动winPython并输入命令:python  
![启动](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/vVFTWHR*NuRY92Gz8eusJJUTjQ0lN3nb9JLIOUYcYXQ!/b/dFMBAAAAAAAA&bo=6QK7AAAAAAADB3I!&rf=viewer_4)
调用sympy函数库，即输入:form sympy import *  (回车键)
然后输入：x = Symbol('x') (回车键)  
最后只需输入：limit(sqrt(x)**(1/sqrt(x)-1),x,1) (回车) 
#### 结果显示为 E ![高数1](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/NurBqzZFIlfEw1gi4ybnWTl1yMzFqEkFoG*70o1ektY!/b/dDEBAAAAAAAA&bo=hgECAYYBAgEDGTw!&rf=viewer_4) 
 ### 2.求y=$\frac{1-x}{1+x}$的微分
输入：integrate((1-x)/(1+x),x)(回车)
![高数2](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/0HD4K8GLHcQHxWWsA5JqoPsqvdAqJjRc1M*G6aVn22E!/b/dDcBAAAAAAAA&bo=hgECAYYBAgEDGTw!&rf=viewer_4)
[LaTeX表示数学符号](http://mohu.org/info/symbols/symbols.htm)    
[一份不太简短的 LATEX 2ε 介绍](http://202.116.81.74/cache/9/03/www.mohu.org/a563578b882a238082752429e17e2a84/lshort-cn.pdf)

## 二·线性代数  


### 1
求$$
 \left[
 \begin{matrix}
  0 & 1 & 4 \\
  1 & 0 & -3 \\
  2 & 3 & 8
  \end{matrix}
  \right]\tag{3}
  $$的逆  
  ![线代1](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/65wnxM9B4ba9Yh8*wHHAn3MkufslF.gntUqR*eHWtrA!/b/dDcBAAAAAAAA&bo=ugH7ALoB.wADGTw!&rf=viewer_4)  
  调用Numpy(NumPy 提供了线性代数函数库 linalg，该库包含了线性代数所需的所有功能)   

  numpy.linalg.inv() 函数计算矩阵的乘法逆矩阵
    
    注释：逆矩阵（inverse matrix）：设A是数域上的一个n阶矩阵，若在相同数域上存在另一个n阶矩阵B，使得： AB=BA=E ，则我们称B是A的逆矩阵，而A则被称为可逆矩阵。注：E为单位矩阵   
  [Numpy 线性代数](http://www.runoob.com/numpy/numpy-linear-algebra.html)   
  ### 2 
  矩阵相乘  
  A=$$
     \left[
     \begin{matrix}
     -1 & 2\\
     5 & 4\\
     2 & -3
     \end{matrix}
     \right]\tag{3}
     $$    

B=$$
     \left[
     \begin{matrix}
      3 & -2\\
     -2 & 1

     \end{matrix}
     \right]\tag{3}
     $$
AB=?  
numpy.dot() 对于两个一维的数组，计算的是这两个数组对应下标元素的乘积和(数学上称之为内积)；对于二维数组，计算的是两个数组的矩阵乘积；对于多维数组，它的通用计算公式如下，即结果数组中的每个元素都是：数组a的最后一维上的所有元素与数组b的倒数第二位上的所有元素的乘积和： dot(a, b)[i,j,k,m] = sum(a[i,j,:] * b[k,:,m])  
![线代2](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/1fEesVl3GFqrm1G2sfrwRAP0xvtyQ1a38U9Y1mWhTS4!/b/dDcBAAAAAAAA&bo=3gEaAd4BGgEDGTw!&rf=viewer_4)  
 [Numpy 线性代数](http://www.runoob.com/numpy/numpy-linear-algebra.html)