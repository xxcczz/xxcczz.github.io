---
layout: default
title: desert-delta
---
## 沙漠三角州
```

# 只攻击在敌军名称(enemyNames)数组中的敌人
# Be sure to attack in order! 0 -> 1 -> 2 -> 3
enemyNames = ["Kog", "Godel", "Vorobun", "Rexxar"]

hero.attack(enemyNames[0])
hero.attack(enemyNames[1])
# 攻击 enemyNames[2]
hero.attack(enemyNames[2])
# 攻击最后一个元素。
hero.attack(enemyNames[3])

```
