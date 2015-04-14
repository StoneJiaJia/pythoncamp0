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

      
    
