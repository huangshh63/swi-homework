# 自顶向下，逐步求精  
## wiki介绍top-down  
自上而下是一种编程风格，是传统程序语言的主流，其中设计从指定复杂的部分开始，然后将它们分成连续的小部分。使用自上而下方法编写程序的技术是编写一个主程序，命名它将需要的所有主要功能。之后，编程团队会查看每个功能的要求，并重复该过程。这些划分的子程序最终将执行如此简单的动作，它们可以轻松简洁地编码。当所有各种子程序都被编码后，程序就可以进行测试了。通过定义应用程序如何在高层次上聚集在一起，较低级别的工作可以是自包含的。通过定义低级抽象如何被整合到更高级别的抽象中  
![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Lego_Chicago_City_View_2001.jpg/1024px-Lego_Chicago_City_View_2001.jpg)  
[TOP-DOWN](https://en.wikipedia.org/wiki/Top-down_and_bottom-up_design#Programming)   
>>维基百科
## 理解  
自顶而下，逐步求精是解决问题有效方法，是将复杂的问题分解开来，分解任务，直至能用很直接的方法。

以洗衣机为案例  
READ 输入水位和时间   


 WHILE (水位小于输入水位)     
       
       打开上水开关注水    
 ENDWHILE   
     
     
     关闭上水开关  
     浸泡一段时间   

REPEAT   
     
     
     电机左转六圈  
     电机右转六圈  
UNTIL 所记时间等于输入时间  

   
   
     停机  

WHILE 水位不降为零   
     
     
     打开排水开关排水  
ENDWHILE    

  关闭排水开关  
IF 衣服干净 THEN  
    
     洗衣成功  
ELSE  
     
      洗衣失败  
ENDIF    
洗衣机洗衣服这一过程可分为很多过程，我们把它先分为几个大的过程，然后再把大过程分解为不能再分为止。  
然而这不能算完，大体写完之后，需要完善细节，删去多余的，补充必要的，用函数解决更小的问题    
在顺序，选择，循环三种结构之中，循环最复杂，但也是解决问题的最有效的结构。  

>>https://blog.csdn.net/sxhelijian/article/details/7303605  
>>https://www.youtube.com/watch?v=QsKkG9gWxF4  
>>http://courses.cs.vt.edu/cs1044/Notes/C02.ProgramDevelopment.pdf