---
layout: default
title: zig-zag-and-zoom
---
## Z字行逃窜
```

# 从死亡峡谷逃出！
# 使用真正的求余函数走出Z字形路线。

# This function returns a value from 0 to 15:
def mod15(n):
    while n >= 15:
        n -= 15
    return n

# 这个函数应该会反馈一个从0到9的值
def mod9(n):
    while n >= 9:
        n -= 9
    return n

# Don't change the following code:
while True:
    time = hero.time
    if time < 30:
        y = 10 + 3 * mod15(time)
    else:
        y = 20 + 3 * mod9(time)
    x = 10 + time
    hero.moveXY(x, y)

```
