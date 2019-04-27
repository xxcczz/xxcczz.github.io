---
layout: default
title: wishing-well
---
## 许愿井
```

# 你需要104的金钱，不多也不少。

less = "Nimis"
more = "Non satis"
requiredGold = 104

# 此函数计算所有的硬币值的总和。
def sumCoinValues(coins):
    coinIndex = 0
    totalValue = 0
    # 遍历所有的金币。
    while coinIndex < len(coins):
        totalValue += coins[coinIndex].value
        coinIndex += 1
    return totalValue

def collectAllCoins():
    item = hero.findNearest(hero.findItems())
    while item:
        hero.moveXY(item.pos.x, item.pos.y)
        item = hero.findNearest(hero.findItems())

while True:
    items = hero.findItems()
    # 获得硬币的总值
    goldAmount = sumCoinValues(items)
    # 如果有金币，那么金币数目 (goldAmount) 不会是零
    if goldAmount != 0:
        # If goldAmount is less than requiredGold
        # 那就说“Non satis”
        if goldAmount<requiredGold:
            hero.say("Non satis")
        # If goldAmount is greater than requiredGold
        # 那么说出“Nimis”。
        if goldAmount>requiredGold:
            hero.say("Nimis")
        # 如果 “goldAmount” 等于 “requiredGold”
        # 如果有刚好 104 金币，就全部收集。
        if goldAmount==requiredGold:
            while True:
                
                item = hero.findNearestItem()
                if item:
                    yidong(item)
        pass
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
