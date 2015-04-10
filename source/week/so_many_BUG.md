##week3作业感想
***
大妈设置的作业让我感受到了深深的挫败感，第一份的作业非常的easy，大家可以根据coursera上的提示来完成，而且导师也详细的说了步骤。第二份作业我以为很简单一开始，自己真正在完成时却是困难重重。以下是我遇到的BUG。

###1.画三角形与正方形
***
这不用说肯定是用canvas作图，按照后面给的例子找到了画三角形的方案，用canvas_draw_polygon()来画，其中的变量是三角形的三个坐标点，当初我的方案是一个点设为pos 那另外三个点就能求出来了。

* 正方形：
       
       
       pos[x,y]
       pos2[0] = pos[0]
       pos2[1] = pos3[1]
       pos3[0] = pos4[0]
       pos4[1] = pos[1]
       pos4[0] - pos[0] = 20
       pos2[1] - pos[1] = 20
       
       
* 三角形：

       pos[x,y]
       pos[0] = (pos3[0]-pos2[0])/2
       pos[1] = pos2[1] - 17.32
       pos2[1] = pos3[1]       
       
于是我运行了一下出现了问题：

      pos4[0] - pos[0] = 20
      SyntaxError: can't assign to operator
之后改变策略
       
      def draw(canvas):
          canvas.draw_polygon([[x,y],[x,y+20],[x+20,y+20],[x+20,y]], 1, "Black", "Red")
          
虽然画出正方形了但没法移动
