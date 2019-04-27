---
layout: default
title: yeti-eater
---
## 雪人食人族
```

# Yetis surround us and we need to defeat them.
# Luckily the wizard had time to cast the sleep spell.
# Your hero can devour the yetis' vital powers when they are defeated.
# Defeat them in the order from weakest to the strongest.

# The wizard sorted enemies, but in the order from the strongest to the weakest.
wizard = hero.findNearest(hero.findFriends())
yetis = wizard.findEnemies()

# You need iterate the yetis list in the reverse order with a 'for-loop'.
# The start value should be 'len(yetis) - 1'.
# Iterate while the index greater than -1.
# Use the negative step -1.
for i in range(len(yetis)-1, -1, -1):
    # Attack each enemy while its health greater than 0.
    yeti=yetis[i]
    while yeti.health>0:
        hero.attack(yeti)
# Look at the guide to get hints.

```
