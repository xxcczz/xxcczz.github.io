---
layout: default
title: snowflakes-on-the-ice
---
## 冰上的雪花
```

def line(start, end):
    # 首先，我们需要得到完整的矢量和幅度，以确定我们是否低于最小阈值。
    full = Vector.subtract(end, start)
    distance = full.magnitude()
    if distance < 4:
        # 如果在我们的阈值距离以下，那么我们将简单地沿矢量绘制一条线并完成（返回告诉我们退出该函数）。
        hero.toggleFlowers(False)
        hero.moveXY(start.x, start.y)
        hero.toggleFlowers(True)
        hero.moveXY(end.x, end.y)
        return
        
    # 否则，我们将通过获得半幅矢量来创建我们的分形。
    half = Vector.divide(full, 2)
    
    # 我们将创建4行分形（开始 - > A，A - > B，B - >和A - >结束），因此我们需要计算中间位置A和B.
    A = Vector.add(half, start)
    
    # 为了得到B，我们需要将矢量旋转90度并乘以2/3（因此它是原始幅度的1/3），然后将其添加到A.
    rotate = Vector.rotate(half, degreesToRadians(90))
    rotate = Vector.multiply(rotate, 2 / 3)
    B = Vector.add(rotate, A)
    
    #现在只需使用线条函数画出4条线。
    line(start, A)
    line(A, B)
    line(B, A)
    line(A, end)
def degreesToRadians(degrees):
    #所有矢量操作都需要以弧度而不是度数工作。
    return Math.PI / 180 * degrees
def flake(start, end):
    # 要创建一个六角片，我们需要创建每次旋转60度的6个线条分形。
    side = Vector.subtract(end, start)
    a = start
    b = end
    for i in range(6):
        line(a, b)
        #为了获得下一个边缘，我们需要将边旋转60度。
        side = Vector.rotate(side, degreesToRadians(60))
        #现在需要重新设置a和b以及新边的开始点和结束点。
        a=b
        b = Vector.add(b,side)
whiteXs = [Vector(12, 10), Vector(60, 10)]
redXs = [Vector(64, 52), Vector(52, 52)]
line(whiteXs[0], whiteXs[1])
flake(redXs[0], redXs[1])

```
