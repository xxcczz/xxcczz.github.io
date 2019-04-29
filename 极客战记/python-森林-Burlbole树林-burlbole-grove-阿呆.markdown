---
layout: default
title: burlbole-grove
---
## Burlbole树林
```

def shouldAttack(target):    
    if not target:    
        return False    
    if target and target.type=="burl":    
        return False    
    return True    
while True:    
    enemy = hero.findNearestEnemy()    
    heroShouldAttack = shouldAttack(enemy)    
    if heroShouldAttack:    
        hero.attack(enemy)

```
