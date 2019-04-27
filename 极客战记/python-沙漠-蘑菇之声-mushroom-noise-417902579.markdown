---
layout: default
title: mushroom-noise
---
## 蘑菇之声
```

# Defeat the skeleton and open the chest.

def onSpawn (event):
    # Pet should find the health potion (type is "potion"): 
    potion = pet.findNearestByType("potion")
    
    
    # and fetch it:
    pet.fetch(potion)
    # Pet should find the gold key (type is "gold-key"):
    goldkey = pet.findNearestByType("gold-key")
    # and fetch it:
    pet.fetch(goldkey)
    pass

# Pet can find more than just items:
skeleton = pet.findNearestByType("skeleton")
pet.on("spawn", onSpawn)
hero.moveXY(44, 18)
hero.moveXY(10, 29)

while True:
    if skeleton.health > 0:
        hero.attack(skeleton)
        
    else:
        hero.moveXY(31, 38)

# Defeat the skeleton and open the chest.

def onSpawn (event):
    # Pet should find the health potion (type is "potion"): 
    potion = pet.findNearestByType("potion")
    # and fetch it:
    if potion:
        pet.fetch(potion)
    # Pet should find the gold key (type is "gold-key"):
    goldkey = pet.findNearestByType("gold-key")
    # and fetch it:
    if goldkey:
        pet.fetch(goldkey)
    pass

# Pet can find more than just items:
skeleton = pet.findNearestByType("skeleton")
pet.on("spawn", onSpawn)

while True:
    if hero.health>1000:
        if skeleton.health > 0:
            hero.attack(skeleton)
        else:
            hero.moveXY(31, 38)

```
