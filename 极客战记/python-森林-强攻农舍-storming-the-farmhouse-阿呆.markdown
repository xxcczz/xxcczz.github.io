---
layout: default
title: storming-the-farmhouse
---
## 强攻农舍
```

# 士兵会慢慢到达，但是食人魔会淹没他们。
# 基本的攻击循环是不能够让你活下来的
while True:
    flag = hero.findFlag()
    enemy = hero.findNearestEnemy()
    if flag:
        hero.pickUpFlag(flag)
        hero.say("也许我应该用旗子干点什么？")
    else:
        hero.shield()

```
