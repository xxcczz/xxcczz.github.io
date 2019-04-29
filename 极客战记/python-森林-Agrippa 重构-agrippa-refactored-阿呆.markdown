---
layout: default
title: agrippa-refactored
---
## Agrippa 重构
```

def cleaveOrAttack(enemy):
    # 如果 “cleave” 技能冷却完毕，那就使用它！否则，使用普通攻击。
    if hero.isReady("cleave"):
        hero.cleave(enemy)
    else:
        hero.attack(enemy)
    pass

while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        distance = hero.distanceTo(enemy)
        if distance < 5:
            # 调用上面定义的 “cleaveOrAttack” 函数
            cleaveOrAttack(enemy)

```
