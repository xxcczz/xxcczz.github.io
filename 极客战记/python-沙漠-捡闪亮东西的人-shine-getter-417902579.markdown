---
layout: default
title: shine-getter
---
## 捡闪亮东西的人
```

# 很快的获取最多的金币

while True:
    coins = hero.findItems()
    coinIndex = 0
    
    # 把这个封装进循环里枚举所有的硬币
    while coinIndex<len(coins):
        coin = coins[coinIndex]
        # 金币价值3点。
        if coin.value == 3:
            # 只捡金币。
            yidong(coin)
            pass
        coinIndex=coinIndex+1
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
