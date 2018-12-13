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
蛇身跟着蛇头而动，这一点很重要，牵一发而动一身，不断坐标交换。  
先进行蛇移动,输出,然后进行判断是否游戏结束，难点是蛇的移动，其他的较好解决;然而又不知道清屏操作，吃了不少苦头，还好请教了别人。
分步考虑，变得简单. 
#### 任务2：会吃的蛇

##### 功能需求：
###### snake 头撞到身体、障碍（边界或你在地图中定义） 游戏结束
###### snake 头吃到食物，snake就长一节
###### 细化并完善随机放置食物的伪代码
###### 找一个空白位置
###### 在该位置放置食物
###### 你需要进一步细化的代码：
###### 蛇头撞到身体、障碍物 … …
###### 蛇头撞到食物 … …
###### 蛇头进入一个空位置 … …    

 

会吃的蛇的难点是如何随机放置食物的位置和当蛇遇到'$'时蛇的变长，这里用到了随机函数rand(),生成两个范围在[1,10]随机数，还要判断是否此时位置为空（这一点有点难以考虑到），再赋予符号'$'，再考虑如果遇到'$'，蛇的长度加一，'$'所在位置变空（这一点也较难）。再进行拆分，直至最简单的步骤。
![会吃的蛇](http://m.qpic.cn/psb?/V12aKRuu4cvTlT/z.xOG.5A6ohXyH6eQRnklLj1vYX9TiJxIBXIVc8LLTE!/b/dLoAAAAAAAAA&bo=lQSOApUEjgICGT0!&rf=viewer_4)
### 实验总结  
确定整体后，再分步考考虑，其中函数的利用恰好反映了自顶而上的思想，大步骤，小问题，使问题变得非常简单,考虑变得简单，也非常利于纠错。  


 附上代码  
   [snake_eat.c](https://github.com/huangshh63/swi-homework/blob/gh-pages/snake_eat.c.md)  
   [snake_move.c](https://github.com/huangshh63/swi-homework/blob/gh-pages/snake_move.c.md)



