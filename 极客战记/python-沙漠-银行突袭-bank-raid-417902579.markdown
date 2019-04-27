---
layout: default
title: bank-raid
---
## 银行突袭
```

# 等待食人魔出现，然后打败它们，并收集金币。

while True:
    coins = hero.findItems()
    # coinIndex is used to iterate the coins array.
    coinIndex = 0
    
    while coinIndex < len(coins):
        # 用 coinIndex 从 coins 数组得到一个金币。
        coin = coins[coinIndex]
        # 收集那个金币。
        hero.moveXY(coin.pos.x, coin.pos.y)
        # 给 coinIndex 的值增加 1。
        coinIndex += 1

```
