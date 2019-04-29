---
layout: default
title: soldier-ogre-and-peasant
---
## 士兵，食人魔和农民
```

# 把这个三位一体交给河的左边。

# 士兵讨厌食人魔。
soldier = pet.findNearestByType("soldier")
# 食人魔计划对农民不利。
ogre = pet.findNearestByType("munchkin")
#只是一个农民。
peasant = pet.findNearestByType("peasant")

# 使用pet.carryUnit（unit，x，y）来交付单位。
pet.carryUnit(ogre, 32, 39)
pet.carryUnit(soldier, 32, 39)
pet.carryUnit(ogre, 49, 40)
pet.carryUnit(peasant, 32, 39)
pet.carryUnit(ogre, 32, 39)

```
