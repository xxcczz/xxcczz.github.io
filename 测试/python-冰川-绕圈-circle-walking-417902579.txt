---
layout: default
title: circle-walking
---
## 绕圈
```

center = Vector(40, 34)
partner = hero.findByType("peasant")[0]
while True:
    vector=Vector.subtract(center,partner.pos)
    moveToPos = Vector.add(center,vector)
    hero.move(moveToPos)

# 镜像你的伴侣围绕中心X标记的动作。
# 向量可以被认为是一个x，y的位置
# 矢量可以反映两个位置之间的距离和方向。

# 使用Vector.subtract（vector1，vector2）查找从vector2到vector1的方向和距离
# 使用Vector.add（vector1，vector2）找到你从vector1到vector2的位置

# 在 X 点的中心创建一个新的 Vector
center = Vector(40, 34)

# 一个单位的位置实际是一个 Vector！
partner = hero.findByType("peasant")[0]

while True:
    # 首先，您要找到伙伴位置到 X 中心的 Vector（距离和方向）。
    vector=Vector.subtract(center,partner.pos)
    
    # 其次，找到你的英雄应该从中心开始移动的位置，并跟随向量。
    moveToPos = Vector.add(center,vector)
    
    # 第三，转移到moveToPos位置。
    hero.move(moveToPos)
    pass

# 在 X 点的中心创建一个新的 Vector
center = Vector(40, 34)

# 一个单位的位置实际是一个 Vector！
partner = hero.findByType("peasant")[0]

while True:
    # 第一，您要找到伙伴位置到 X 中心的 Vector（距离和方向）。
    vector=Vector.subtract(center,partner.pos)
    
    # 第二，找到你的英雄应该移动的位置，从中心开始，然后跟随向量。
    moveToPos = Vector.add(center,vector)
    
    # 第三，移动到moveToPos位置
    hero.move(moveToPos)

```
