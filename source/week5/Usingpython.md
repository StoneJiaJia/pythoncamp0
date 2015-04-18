##Designing and Using Functions
****
###方程
比如abs（-9）= 9
绝对值

round（3.8）= 4
离数值越近的整数

pow（2，4）= 16   指的是2^4

还有 min（）max（）等等

 

    >>> int(34.6)
    34
    >>> int(-4.3)
    -4
    >>> float(21)
    21.0

如果你不确定方程的用途的话可以用help来了解


       
    >>> help(abs)
    Help on built-in function abs in module builtins:
    abs(...)
    abs(number) -> number
    Return the absolute value of the argument.

第三行是这方程的一般形式，括号内是数字，输出的也是数字
最后一行说明这个方程是求平均值的

又比如
       
       >>> help(pow)
      Help on built-in function pow in module builtins:
      pow(...)
          pow(x, y[, z]) -> number
          With two arguments, equivalent to x**y.  With    three arguments,
          equivalent to (x**y) % z, but may be more efficient (e.g. for longs).

告诉我们pow不仅可以用来做幂运算，第三个还能用作求余数。


###python如何来追踪数值

python为了追踪每个数值，都赋予了他们每个id

          >>> help(id)
      Help on built-in function id in module builtins:
      id(...)
          id(object) -> integer
          Return the identity of an object.  This is guaranteed to be unique among
          simultaneously existing objects.  (Hint: it's the object's memory
          address.)
     How cool is that? Let’s try it:
      >>> id(-9)
      4301189552
      >>> id(23.1)
      4298223160
      >>> shoe_size = 8.5
      >>> id(shoe_size)
      4298223112
      >>> fahrenheit = 77.7
      >>> id(fahrenheit)
      4298223064

不仅如此，方程也有自己的id
    
      >>> id(abs)
      4297868712
      >>> id(round)
      4297871160
###定义我们自己的方程
BMI是身高体重指数，方程式是 BMI = （w/h^2）
按照之前的模式我们希望只要输入我们的体重和身高就能输出我们自己的BMI了
BMI（weight， height）

     >>>BMI(90, 1.79)
     28.089010954714272
     
我BMI值是28属于肥胖了，需要减肥了
当然现在BMI值还没存在在我们的python中需要我们定义，直接输入BMI的话会出现   
     
     >>>BMI(90, 1.79)
     Traceback (most recent call last):
     File "<stdin>", line 1, in <module>
     NameError: name 'convert_to_celsius' is not defined  

这样的错误

那现在我们来定义BMI值吧

    >>> def BMI(weight, height):
    ...     return weight/(height**2)
这里我们需要注意的是

 * return要首行缩进4个空格建
 * 没法定义数字 def = 3
 * 不能定义python中已有的关键词 def = return（x）
   
         False assert del for None break elif from True class else global and continue except if
        as def finally import
        in or
        is pass lambda raise nonlocal return not try
        while with yield

###Using Local Variables for Temporary Storage

********


      >>> def quadratic(a, b, c, x):
      ... first=a*x**2
      ... second=b*x
      ... third = c
      ...     return first + second + third
      ...
      >>> quadratic(2, 3, 4, 0.5)
      6.0
      >>> quadratic(2, 3, 4, 1.5)
      13.0

这例子中我们为了能简化return的函数，可以在这个方程中自己定义first， second，third。最后输出的值是这三个定义的值的函数。
但之后我们发现，如果定义好方程后再写代码时，python不会追踪到你之前在上个方程中所定义的first
   
       >>> first
      Traceback (most recent call last):
        File "<stdin>", line 1, in <module>
      NameError: name 'first' is not defined

 这是因为方程内定义的first只适应与这方程自己。

 这是因为python执行一个方程时就好像又重开了一个python，你所定义的first在另外一个python程序中

      
