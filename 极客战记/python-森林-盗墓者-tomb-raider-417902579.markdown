---
layout: default
title: tomb-raider
---
## 盗墓者
```

# 森林中一座被遗忘的墓地！
# 但是食人魔紧追不舍。
# 在防御矮人的同时破开坟墓

# 这个函数应该在敌人存在时攻击，否则攻击门！
def checkToDefend(target):
    # 检查目标是否存在
    if target:
        hero.attack(target)
        # 如果是这样，攻击目标。
    else:
        hero.attack("Door")
    # 如果没有目标，使用else去做点别的事
    
        # 否则攻击 "Door"
        
    pass

while True:
    enemy = hero.findNearestEnemy()
    checkToDefend(enemy)

```
