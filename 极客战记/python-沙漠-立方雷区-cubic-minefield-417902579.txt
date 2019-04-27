---
layout: default
title: cubic-minefield
---
## 立方雷区
```

# 穿过雷区

# 这个函数返回乘以次数的数字。
def mult(number, times):
    total = 0
    while times > 0:
        total += number
        times -= 1
    return total

# 这个函数返回乘方的数字。
def power(number, exponent):
    total = 1
    # 补全函数。
    while exponent > 0:
        total =total*number
        exponent -= 1
    return total

# 别修改这些代码
# You can find coefficients for the equation on the tower
tower = hero.findFriends()[0]
a = tower.a
b = tower.b
c = tower.c
d = tower.d
x = hero.pos.x

while True:
    # To find the path use a cubic equation
    y = a * power(x, 3) + b * power(x, 2) + c * power(x, 1) + d * power(x, 0)
    hero.moveXY(x, y)
    x = x + 5

```
