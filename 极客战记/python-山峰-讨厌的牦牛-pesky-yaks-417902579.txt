---
layout: default
title: pesky-yaks
---
## 讨厌的牦牛
```

# 一大群牦牛
# 如果生存，你需要过滤掉牦牛
def removeByType(enemies, excludedType):
    tempList = []
    # 经过并检查每一个敌人是否excludedtype
    for enemy in enemies:
        # 如果它不是，添加进列表
        if enemy.type!=excludedType:
            tempList.append(enemy)
        pass
    return tempList

while True:
    # 找到敌人
    enemies = hero.findEnemies()
    # 清除那些讨厌的牦牛
    enemies = removeByType(enemies, "sand-yak")
    enemy = hero.findNearest(enemies)
    if enemy:
        # 现在...“清除”那些敌人
        hero.attack(enemy)

```
