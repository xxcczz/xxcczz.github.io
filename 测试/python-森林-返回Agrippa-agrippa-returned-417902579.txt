---
layout: default
title: agrippa-returned
---
## 返回Agrippa
```

def enemyInRange(enemy):
    # 如果敌人少于5个单位，返回一个true值
    if hero.distanceTo(enemy)<5:
        return True
    else:
        return False

def cleaveOrAttack(enemy):
    if hero.isReady('cleave'):
        hero.cleave(enemy)
    else:
        hero.attack(enemy)

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        # 调用 enemyInRange 检查敌人的距离。
        if enemyInRange(enemy):
            cleaveOrAttack(enemy)

```
