###python 球的运动
***

首先需要画了球，我们能选择球的大小和半径，用canvas.draw_circle 就行
vel = [x, y]表示球是每次沿x轴运动的个数和Y轴运动的个数。
      
       当前坐标D是[x,y],[6,1]表示坐标D变成[x+6,y+1]
       
####介绍两种球移动的代码
*  先定义时间和创建球的list，如果不创建球的list的话，运行时会出现ball_pos Not define的提示
 
  
          #define event handlers
          def tick():
          global time
          time = time + 1

          def draw(canvas):
          # create a list to hold ball position
          ball_pos = [0, 0]

          # calculate ball position
          ball_pos[0] = init_pos[0] + time * vel[0]
          ball_pos[1] = init_pos[1] + time * vel[1]
    
          # draw ball
          canvas.draw_circle(ball_pos, BALL_RADIUS, 2, "Red", "White")
