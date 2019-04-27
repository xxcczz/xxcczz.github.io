---
layout: default
title: greed-traps
---
## 贪婪的陷阱
```

# 巡逻并只在看到金币时设置陷阱。

# 编写这个函数
def maybeBuildTrap(x, y):
    # 移动到给定的xy位置
    hero.moveXY(x, y)
    # 搜寻一枚硬币，如果找到就建造一个"fire-trap"
    item = hero.findNearestItem()
    if item:
        hero.buildXY("fire-trap", x, y)
    pass

while True:
    # 为左上方通道调用maybeBuildTrap
    maybeBuildTrap(12, 56)
    # 下面是右上角的通道。
    maybeBuildTrap(68, 56)
    # 下面是右下的通道。
    maybeBuildTrap(68, 12)
    # 下面是左下角的通道。
    maybeBuildTrap(12, 12)

```
