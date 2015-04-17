###Designing New Functions: A Recipe
写出好的文章需要计划，决定一个主题，了解主题的背景和材料，写提纲，补充你写的提纲。同样的写好一个方程也需要计划，你要知道你需要方程干什么事，怎么命名你的方程，有哪些参数，怎么return。下面有个例子： 
    
    >>> def days_difference(day1, day2):
      ...     """ (int, int) -> int
      ...
      ...     Return the number of days between day1 and                         day2, which are
      ...     both in the range 1-365 (thus indicating the day of the
      ... year).
      ...
      ...     >>> days_difference(200, 224)
      ... 24
      ...     >>> days_difference(50, 50)
      ... 0
      ...     >>> days_difference(100, 99)
      ... -1
      ... """
      ...     return day2 - day1
      ...

* 第一行是方程的开头

* 第二行说明有那几个参数，和参数的特性（int还是float），并且输出的是数字和数字的特性

* 之后是方程要将要做的事和什么时候要求做和 what the function returns.

* 下一个是写例子，方程中输入参数返回的值

* 最后一个是方程的核心

###写好方程的六个步骤

***

* 构思出你想用哪些信息并能输出一个你想要的数值，选择一个短语来命名你的方程做好能看出这方程是干什么的短语。

比如
     

     ...     >>> days_difference(200, 224)
     ... 24
     ...     >>> days_difference(50, 50)
     ... 0
     ...     >>> days_difference(100, 99)
     ... -1

* 决定你的信息的特性和输出的值的特性

* 写方程的开头一部分，最好选择一个有意义的短语来命名    

* 描述你想要输出的值是什么，来了解自己写的方程的目的

* 写方程的核心，他能输出的值是你想要的。

：return BMI = （weight/height**2）

* 测试自己的方程是否正确
