---
layout: default
title: key-traps
---
## 钥匙陷阱
```

# Get three keys and free the paladin.

def onSpawn(event):
    # The pet should find and fetch three keys.
    # You need items with the next types:
    # "bronze-key", "silver-key" and "gold-key".
    a = pet.findNearestByType("bronze-key")
    pet.fetch(a)
    b = pet.findNearestByType("silver-key")
    pet.fetch(b)
    c = pet.findNearestByType("gold-key")
    pet.fetch(c)
pet.on("spawn", onSpawn)

while True:
    enemy = hero.findNearestEnemy()
    if enemy and enemy.team == "ogres":
        hero.attack(enemy)
    if hero.health < 300:
        # You can use pets in the main thread too.
        potion = pet.findNearestByType("potion")
        if potion:
            hero.moveXY(potion.pos.x, potion.pos.y)

```
