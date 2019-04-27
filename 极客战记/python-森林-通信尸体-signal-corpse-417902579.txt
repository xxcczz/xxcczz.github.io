---
layout: default
title: signal-corpse
---
## 通信尸体
```

# 你可以使用旗子来选择不同的策略
# 在这关，绿色旗子代表你要移动到旗子处。
# 遇到黑旗就意味着你要劈开旗子
# The doctor will heal you at the Red X

while True:
    green = hero.findFlag("green")
    black = hero.findFlag("black")
    nearest = hero.findNearestEnemy()
    
    if green:
        hero.pickUpFlag(green)
    elif black and hero.isReady("cleave"):
        hero.pickUpFlag(black)
        # 劈斩！
        hero.cleave(nearest)
    elif nearest and hero.distanceTo(nearest) < 10:
        # 攻击！
        hero.attack(nearest)
        pass

```
