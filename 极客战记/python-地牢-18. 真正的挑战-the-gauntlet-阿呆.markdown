---
layout: default
title: the-gauntlet
---
## 18. 真正的挑战
```

# 使用你刚学到的技能击败那些食人魔。
# 记住：打败食人魔矮人需要两次攻击。
while True:
    enemy=hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)
    else:
        hero.moveRight()

# 使用你刚学到的技能击败那些食人魔。
# 记住：打败食人魔矮人需要两次攻击。
while True:
    hero.moveRight()
    enemy = hero.findNearestEnemy()
    hero.attack(enemy)
    hero.attack(enemy)

```
