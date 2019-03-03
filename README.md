# Pikaqiu 用turtle绘画的皮卡丘

1. 首先我们导入turtle库和time库（用来做动画使用）:
```
import turtle as t
import time
```
2. 由于turtle没有画曲线的函数，因此我们自定义画曲线函数,函数有4个参数，ang偏转角度，dis移动步长，step步长增幅，n遍历次数，说白了就是将曲线转化为很多条短长的直线：
```
#画左偏曲线函数
def radian_left(ang,dis,step,n):
    for i in range(n):
        dis+=step #dis增大step
        t.lt(ang) #向左转ang度
        t.fd(dis) #向前走dis的步长
        
def radian_right(ang,dis,step,n):
    for i in range(n):
        dis+=step
        t.rt(ang) #向左转ang度
        t.fd(dis) #向前走dis的步长
```
3. 定义画耳朵，眼睛，嘴，轮廓，脚画尾巴的函数，具体见python文件
4. 初始化皮卡丘：
```
#初始化
def Init():
    InitEars()
    InitTail()
    InitFoots()
    InitBody()
    InitFace()
    InitHands()
    InitEyes()
```
5. 定义Upgrade函数和Upgarde_init函数制作眨眼动画：
```
#眨眼睛
def Upgarde():
    InitEars()
    InitTail()
    InitFoots()
    InitBody()
    InitFace()
    InitHands()
    CloseEyes()
 
def Upgarde_Init():
    InitEars()
    InitTail()
    InitFoots()
    InitBody()
    InitFace()
    InitHands()
    InitEyes()
 ```
 6. Main函数定义：
 ```
 def main():

    Init()
    
    t.tracer(False)
    
    #眨眼睛动画
    for i in range(30):
        if i%2==0:
            t.reset()
            t.hideturtle()
            Upgarde()
            t.update()
            time.sleep(0.3)
        else:
            t.reset()
            t.hideturtle()
            Upgarde_Init()
            t.update()
            time.sleep(1)        
```
#展示
