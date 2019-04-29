---
layout: default
title: gas-attack
---
## 毒气攻击
```

# Calculate the total health of all the ogres.

def sumHealth(enemies):
    # 创建一个变量，将它设为0后开始运算
    totalHealth = 0
    index=0
    # Initialize the loop index to 0
    while index<len(enemies):
        
        # 虽然索引小于敌人数组的长度
        
        # Add the current enemy's health to totalHealth
        totalHealth=totalHealth+enemies[index].health
        # 让 index 递增
        index=index+1

    return totalHealth

# Use the cannon to defeat the ogres.
cannon = hero.findNearest(hero.findFriends())
# The cannon can see through the walls.
enemies = cannon.findEnemies()
# Calculate the sum of the ogres' health.
ogreSummaryHealth = sumHealth(enemies)
hero.say("使用 " + ogreSummaryHealth + " 克。")

```
