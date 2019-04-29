---
layout: default
title: grid-minefield
---
## 网格雷区
```

#一个食人魔队正朝着村庄前进。
#我们为我们的“客人”准备了很多会议。
#我们会用他们严格的形式对付他们！
#如果我们将矿井放置在食人魔的阵线之间，并且一次冲击它#们，
#食人魔将飞行使用嵌套循环来建立网格雷区，
#但是，数量增加比一个更大，并使用这些坐标来放置地雷！
#除非人类踩到它们，否则这些地雷不会爆炸，
#所以不要害怕，迈出一步！
# 食人魔队正在村庄前进。
# 我们有90秒时间来建造雷区。
# 我们会用他们严格的阵型对付他们。

#使用嵌套循环来构建网格雷区。
# 首先用步骤8重复从12到60的x坐标。
for x in range(12, 12 + 8 * 6, 8):
    # 对于每个x迭代y坐标从12到68与步骤8。
    for y in range(12, 12 + 8 * 7, 8):
        # 为每个点建立“。 "fire-trap" there.
        hero.buildXY("fire-trap", x, y)
        pass
    # 在每一栏之后，最好向右移动避开自己的陷阱。
    hero.moveXY(hero.pos.x + 8, hero.pos.y)

#现在等待并观察即将到来的食人魔。
# 当他们靠近（距离英雄约20米）时，与你的英雄一起开采地雷。
#只要在最近的矿井移动即可。
while True:    
    enemy = hero.findNearestEnemy()
    if enemy:
        distance1 = hero.distanceTo(enemy)
        if distance1<20:
            hero.moveXY(52, 52)

```
