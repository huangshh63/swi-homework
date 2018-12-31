# 利用机器指令控制冯诺依曼计算机执行程序。

## 一、实验目的
### 理解冯·诺伊曼计算机的结构
### 理解机器指令的构成
### 理解机器指令执行周期
### 用汇编编写简单程序
## 二、实验/学习工具
### 简单 CPU 仿真工具 Pippin CPUSim ！
![Pippin](http://a1.qpic.cn/psb?/V12aKRuu4cvTlT/o09iSrhaVaZsxRPVJ7bXJhj1nwe8yD36a0e58HFefKU!/m/dLgAAAAAAAAAnull&bo=iAIrAgAAAAACB4A!&rf=photolist&t=5)
### 实验环境环境

#### windows 7 或 以下
#### 浏览器 IE 8 或 以下
#### Java Runtime Environment 1.6（JRE 6.0）或 以下网址
#### http://www.science.smith.edu/~jcardell/Courses/CSC103/CPUsim/cpusim.html
#### 如果你的设备不符合以上要求，则需要安装虚拟机  
![xpxp](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/yXBdliZTUHa5sNdctSB1rpBARXOTDvbW11k0j0kw6s8!/b/dL8AAAAAAAAA&bo=iAIrAgAAAAACN7A!&rf=viewer_4)  
## 三实验步骤  
### 任务一  
#### （1）打开网页 The PIPPIN User’s Guide ，然后输入 Program 1：Add 2 number  
![cpu](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/u7HD*Hha*MS9zW78kQkdh14Gvo2psTNdMrPGxewUyf8!/c/dLwAAAAAAAAA&bo=iQKhAQAAAAACFxg!&rf=viewer_4)
#### （2）点step after step。观察并回答下面问题：
![cpu1](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/4xshPcBBxHxnnLyGO3n7J8y9B0D0xi1V0IKTnEuO18Q!/c/dL8AAAAAAAAA&bo=iQKhAQAAAAACFxg!&rf=viewer_4)
![dd](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/0hcadRw2d.Dnles.JXvIZon34QvVqTR8Mu*vAeXvC2I!/b/dL8AAAAAAAAA&bo=YQJ4AQAAAAADFyg!&rf=viewer_4)  

##### PC，IR 寄存器的作用。  
IR 指令寄存器 存放当前从主存储器读出的正在执行的一条指令。   
![IR](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/45WXAXB6lct86OBYpBzzueMKkdL41Rfei1YZ*ICrCTE!/b/dL8AAAAAAAAA&bo=lAAlAAAAAAADF4M!&rf=viewer_4) 
PC 程序计数器 存放下一条指令所在单元的地址的地方     
![pc](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/mK1YFvhsP*C2jUX8RrmvP4oWL4ksOGpkxO*SZAKZnMs!/b/dFMBAAAAAAAA&bo=VgA5AAAAAAADF10!&rf=viewer_4)
##### ACC 寄存器的全称与作用。
Accumulator  
存放操作数或运算结果  
##### 用“LOD #3”指令的执行过程，解释Fetch-Execute周期。  
![lod#3](http://a4.qpic.cn/psb?/V12aKRuu4cvTlT/7yhrxOl2cGofAAacrQlbMXcL1AYl0z6m*SwStOX0C*s!/m/dDMBAAAAAAAAnull&bo=iQKhAQAAAAACBwg!&rf=photolist&t=5)
##### 用“ADD W” 指令的执行过程，解释Fetch-Execute周期。
![w1](http://a3.qpic.cn/psb?/V12aKRuu4cvTlT/WJBmzJaMqf2wNtj1tbjEyM7G.UBeRkxhHg43d19FNyY!/m/dL4AAAAAAAAAnull&bo=iQKhAQAAAAACBwg!&rf=photolist&t=5)    
![w2](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/aZPKOSCVj.wi0JkzeNnHG1dPMI7fvsZxjeXEbvDiS04!/c/dL8AAAAAAAAA&bo=iQKhAQAAAAACBwg!&rf=viewer_4)

##### “LOD #3” 与 “ADD W” 指令的执行在Fetch-Execute周期级别，有什么不同。
前者没有get data.
#### （3）点击“Binary”,观察回答下面问题

##### 写出指令 “LOD #7” 的二进制形式，按指令结构，解释每部分的含义。  
00010100 00000111  
##### 解释 RAM 的地址。  
![RAM](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/RsKc6cp.PlsgEHA202oIQecgvTSkiHlRh94BbQuo8VI!/b/dDcBAAAAAAAA&bo=wwE5A8MBOQMDCSw!&rf=viewer_4)

#### 该机器CPU是几位的？（按累加器的位数） 
8位
#### 写出该程序对应的 C语言表达。  
int x=3;
int w=7;  
int y=w+z;  
## 任务 2：简单循环

#### （1） 输入程序Program 2，运行并回答问题：

##### 用一句话总结程序的功能
1~10的循环
##### 写出对应的 c 语言程序
     int x=1;
    while(x<11>){
    
    x++;
    }
#### （2） 修改该程序，用机器语言实现 10+9+8+..1 ，输出结果存放于内存 Y

##### 写出 c 语言的计算过程
int x=1,y=0;
while(x<11){
    y+=x;
    x++;
}  
![10+9+..+1](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/5c7mUjd*34cBdGGAWObNTsoByNl94TvfHtsxmWkpv9k!/c/dMIAAAAAAAAA&bo=iQKhAQAAAAACJyg!&rf=viewer_4)
##### 写出机器语言的计算过程
![jiqiyuyan](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/Q8W4ls9S1jnyuUzvQO9mUB0oXEsRwtVP29JEoMlaUVU!/b/dL8AAAAAAAAA&bo=fwB8AAAAAAADByE!&rf=viewer_4)
##### 用自己的语言，简单总结高级语言与机器语言的区别与联系。
机器语言是计算机能够直接识别的，而高级语言对计算机来说是不能直接识别的，需被翻译成汇编语言再由汇编语言汇编成机器语言之后，在被执行。  
## 实验小结  
总体上，实验目的基本达成，无论是实验环境准备，还是实验的进行，都有着不错的表现，更加深入的理解冯·诺伊曼计算机的结构。