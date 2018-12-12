## 字符游戏 - 贪吃蛇实验报告  
### 一.实验目的
1.了解字符游戏的表示
  
2.体验自顶向下的设计方法实现问题求解

3.使用伪代码表示算法

4.使用函数抽象过程  
### 实验内容

#### 会动的蛇
##### 程序头部要求定义良好的头部，将使得程序更加易于阅读，易于维护。包括：常数定义、函数定义等。你需要参照以下内容，设计你程序的头部：
![123](https://sysu-swi.github.io/images/snake-head.png)
 ##### 程序总体结构必须严格符合以下伪代码框架 :
    输出字符矩阵
	WHILE not 游戏结束 DO
		ch＝等待输入
		CASE ch DO
		‘A’:左前进一步，break 
		‘D’:右前进一步，break    
		‘W’:上前进一步，break    
		‘S’:下前进一步，break    
		END CASE
		输出字符矩阵
	END WHILE
	输出 Game Over!!! 
会动的蛇效果演示图
![演示图](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/yaJV04Ki.PHJyx7ALw64Zb.dvEM5p5K6LyzrBnSIwN8!/b/dFQBAAAAAAAA&bo=lQSOApUEjgICKQ0!&rf=viewer_4)
![1](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/RMPd6DiXQPyM0I3CNer*wY2qxwadMRiMwsrC*8A3QEI!/b/dL8AAAAAAAAA&bo=.QHXAvkB1wIDGTw!&rf=viewer_4) 
![2](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/ERZWZqirmigf1PhHjCReNbLUuAkFmK4LI2AwlAy7OYg!/b/dL8AAAAAAAAA&bo=EwK9AhMCvQIDGTw!&rf=viewer_4)
![3](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/U8rSuitMXu0Dzv0Qjw7n*i7..ExhzesXyIHrPnJ0Juc!/b/dLYAAAAAAAAA&bo=wgHMAcIBzAEDGTw!&rf=viewer_4)

