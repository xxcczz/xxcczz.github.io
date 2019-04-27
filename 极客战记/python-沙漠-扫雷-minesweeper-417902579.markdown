---
layout: default
title: minesweeper
---
## 扫雷
```

# 让农民和他们的拯救者通过雷区。

while True:
    coin = hero.findNearestItem()
    healingThreshold = hero.maxHealth / 2
    # Check to see if you are critically injured.
    if hero.health < healingThreshold:
        # Move left 10m.
        
        # Ask for a heal.
        hero.say("Can I get a heal?")
        pass
    # Else, move to the next coin.
    elif coin:
        hero.moveXY(coin.pos.x, coin.pos.y)

```
