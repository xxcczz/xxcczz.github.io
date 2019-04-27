---
layout: default
title: lost-viking
---
## 失落的维京
```

# 你必须点击帮助按钮查看本关的详细描述

# 乌鸦会告诉你这些迷宫的参数都是什么用处！

# 你已经向北走了多少sideSteps，距离红色X 标记。
sideSteps = 1

# 你已经向东走了多少步，距离红色X 标记。
steps = 1

# 用步数乘以这个来确定你的 X 坐标，别修改这个！
X_PACE_LENGTH = 4

# 用sideSteps成衣这个来确定你的 Y 坐标，别修改这个！
Y_PACE_LENGTH = 6
bl1=0
bl2=0
fx=1
slide=8
switch=6
skip=11
c=0
# 这个迷宫在 X 方向有35步
while steps <= 35:
    hero.say("第"+steps+"步")
    a=steps * X_PACE_LENGTH
    b=sideSteps * Y_PACE_LENGTH*fx
    if steps==skip:
        b=c+2*fx
    hero.say("坐标:"+a+","+b)
    d=b-c
    hero.say("纵坐标增加值:"+d)
    # 进行下一步：
    if d>slide:
        b=1
        hero.say(a+","+b)
    if d<-slide:
        b=c-slide
        hero.say("纵坐标增加值修正:"+-slide)
        hero.say(a+","+b)
    c=b
    hero.moveXY(a, b)
    
    # 根据特殊规则，增加合适的步数和 sideSteps
    steps += 1
    sideSteps=sideSteps+1
    if steps-switch*bl2>switch:
        bl2=bl2+1
        fx=fx*-1

hero.moveXY(5, 1)
enemy = hero.findNearestEnemy()
if enemy:
    hero.attack(enemy)
    hero.attack(enemy)
    hero.attack(enemy)
    x=0
    y=0
x=70
y=20
hero.moveXY(x,y)
hero.say(x+","+y)
x=140
y=20
hero.moveXY(x,y)
hero.say(x+","+y)
x=140
y=50
hero.moveXY(x,y)
hero.say(x+","+y)

hero.moveXY(1, 7)
enemy = hero.findNearestEnemy()
hero.attack(enemy)
hero.say("message")
hero.moveXY(1, 1)
x=0
y=0
x=70
y=20
hero.moveXY(x,y)
hero.say(x+","+y)
x=140
y=20
hero.moveXY(x,y)
hero.say(x+","+y)
x=140
y=50
hero.moveXY(x,y)
hero.say(x+","+y)

```
