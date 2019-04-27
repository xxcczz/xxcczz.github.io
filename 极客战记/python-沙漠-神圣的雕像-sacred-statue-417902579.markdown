---
layout: default
title: sacred-statue
---
## 神圣的雕像
```

# 沿着食人魔的营地周边的点走，干掉遇到的所有敌人。
# 查看雕像开始本关。
# 站好，击败进攻的食人魔。

# 提示：在战斗中距离雕像近的战斗会有它的帮助

# 在你击败了所有波食人魔后，你有机会与远古的Cyclops对决！
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    else:
        hero.moveXY(62, 62)
        hero.shield()
        
```
