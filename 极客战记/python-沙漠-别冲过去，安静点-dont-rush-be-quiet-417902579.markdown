---
layout: default
title: dont-rush-be-quiet
---
## 别冲过去，安静点
```

# Dodge the cannons and collect 8 gems.
# Watch out, cannons are ready to fire!
# 以一个特殊的方式缓慢移动去迷惑敌人

# This function returns a value from 0 to 30:
def mod30(n):
    if n >= 30:
        return n - 30
    else:
        return n

# 这一功能将会返回一个从0到40的值
def mod40(n):
    # 使用一个 “if” 语句去返回正确的值
    if n >= 40:
        return n - 40
    else:
        return n

# You don't need to change the following code:
while True:
    time = hero.now()
    x = mod30(time) + 25
    y = mod40(time) + 10
    hero.moveXY(x, y)

```
