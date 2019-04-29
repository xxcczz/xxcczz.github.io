---
layout: default
title: medical-attention
---
## 医疗注意
```

# 当你生命值少于一半时，请求医疗人员的治疗。

while True:
    currentHealth = hero.health
    healingThreshold = hero.maxHealth / 2
    # 如果你当前的健康值少于下限，
    # move to the healing point and say, "heal me".
    # 否则的话，攻击。你需要战斗的更狠点！
    if currentHealth<healingThreshold:
        hero.moveXY(65, 47)
        hero.say("heal me")
    else:
        gongji()
def gongji():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
