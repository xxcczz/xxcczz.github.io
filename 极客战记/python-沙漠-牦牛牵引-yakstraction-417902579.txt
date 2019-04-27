---
layout: default
title: yakstraction
---
## 牦牛牵引
```

# 保护 brandy 避免那些冲来的口渴的耗牛！
# 收集金币来建造诱饵干扰耗牛。
# 使用旗子来决定什么时候在哪里建造诱饵。
while True:
    flagGreen = hero.findFlag("green")
    flagBlack = hero.findFlag("black")
    
    if flagGreen:
        hero.pickUpFlag(flagGreen)
    if flagBlack:
        hero.pickUpFlag(flagBlack)
        hero.buildXY("decoy", flagBlack.pos.x, flagBlack.pos.y)

```
