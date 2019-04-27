---
layout: default
title: skating-away
---
## 滑走
```

#避开牦牛移动到红色的X标记。
# 使用Vector.normalize（vector1）创建一个与vector1相同方向的向量，但距离为1
# 使用Vector.multiply（vector1，X）创建一个与vector1相同方向的向量，但其距离乘以X

# 你想要的点。
goalPoint = Vector(78, 34)

while True:
    # 这会创建一个向量，将您移动到目标点10米
    # 首先，从你的英雄到目标点创建一个向量。
    goal = Vector.subtract(goalPoint, hero.pos)
    # 然后，将它归一化为1米距离矢量
    goal = Vector.normalize(goal)
    # 最后，将1m矢量乘以10，得到一个10m长的矢量。
    goal = Vector.multiply(goal, 10)
    
    #为了避免牦牛，如果你距离牦牛10米以内，你应该远离牦牛。
    yak = hero.findNearest(hero.findEnemies())
    distance = hero.distanceTo(yak)
    if distance < 10:
        # 首先，从牦牛向你制作一个Vector
        vector=Vector.subtract(hero.pos,yak.pos)
        #现在使用Vector.normalize和Vector.multiply使它长10米
        vector = Vector.normalize(vector)
        vector = Vector.multiply(vector, 10)
        # 从牦牛身上取出10米的矢量后，使用Vector.add将其添加到您的目标矢量中！
        goal = Vector.add(goal,vector)
        pass
    
    # 最后，通过将目标向量添加到当前位置来确定移动的位置。
    moveToPos = Vector.add(hero.pos, goal)
    hero.move(moveToPos)

goalPoint = Vector(78, 34)
while True:
    goal = Vector.subtract(goalPoint, hero.pos)
    goal = Vector.normalize(goal)
    goal = Vector.multiply(goal, 10)
    yak = hero.findNearest(hero.findEnemies())
    distance = hero.distanceTo(yak)
    if distance < 10:
        goal1=Vector.subtract(hero.pos,yak.pos)
        goal = Vector.add(goal,goal1)
        pass
    moveToPos = Vector.add(hero.pos, goal)
    hero.move(moveToPos)

# Move to the red X mark while avoiding the yaks.
# use Vector.normalize(vector1) to create a vector in the same direction as vector1, but with a distance of 1
# use Vector.multiply(vector1, X) to create a vector in the same direction as vector1, but with its distance multiplied by X

# The point you want to get to.
goalPoint = Vector(78, 34)

while True:
    # 这会创建一个向量，将您移动10米到达目标点
    # 首先，创建一个矢量从你的英雄向目标点。
    goal = Vector.subtract(goalPoint, hero.pos)
    # 然后，将其归一化为1m距离向量。
    goal = Vector.normalize(goal)
    # 最后，将1m矢量乘以10，得到一个10m长的矢量。
    goal = Vector.multiply(goal, 10)
    
    # 为了避免牦牛，如果你距离牦牛10米以内，你应该远离它。
    yak = hero.findNearest(hero.findEnemies())
    distance = hero.distanceTo(yak)
    if distance < 10:
        # 首先，创建一个从耗牛向你的矢量
        goal1 = Vector.subtract(hero.pos, yak.pos)
        # 现在使用Vector.normalize和Vector.multiply使它长10米
        goal1 = Vector.normalize(goal1)
        goal1 = Vector.multiply(goal1, 10)
        # 一旦你有了距离牦牛10米的矢量，使用Vector.add将它添加到你的目标矢量！
        goal = Vector.add(goal,goal1)
        pass

    # 最后，通过将目标向量添加到当前位置来确定移动的位置。
    moveToPos = Vector.add(hero.pos, goal)
    hero.move(moveToPos)

```
