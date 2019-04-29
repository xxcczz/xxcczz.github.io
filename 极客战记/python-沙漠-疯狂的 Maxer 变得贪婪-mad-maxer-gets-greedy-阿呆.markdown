---
layout: default
title: mad-maxer-gets-greedy
---
## 疯狂的 Maxer 变得贪婪
```

# 比你的分身收集的金币多。
# 你只有几秒钟来收集金币，聪明的选择你的路线！
while True:
    bestCoin = None
    maxRating = 0
    coinIndex = 0
    coins = hero.findItems()
    # 试着计算"价值/距离"来决定你要收集哪个金币。
    jianjinbi()
    
def jianjinbi():
    items = hero.findItems()
    a=None
    maxjz=0
    for item in items:
        if item.pos.x>40:
            continue
        jz=item.value/hero.distanceTo(item)
        if jz>maxjz:
            maxjz=jz
            a=item
    if a:
        hero.move(a.pos)

```
