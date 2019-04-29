---
layout: default
title: key-stack
---
## 密钥栈
```

// Open doors and collect treasures.

var peasant = hero.findByType("peasant")[0];

var goldKey = peasant.findByType("gold-key")[0];
var silverKey = peasant.findByType("silver-key")[0];
var bronzeKey = peasant.findByType("bronze-key")[0];

// Command the peasant to pick up the gold and silver keys.
hero.command(peasant, "pickUpItem", goldKey);
hero.command(peasant, "pickUpItem", silverKey);
// Now, command the peasant to pick up the last key:
hero.command(peasant, "pickUpItem", bronzeKey);

// Command the peasant to drop a key near the first door.
hero.command(peasant, "dropItem", {x: 40, y: 34});
// The second key -> the second door.
hero.command(peasant, "dropItem", {x: 31, y: 34});
// Drop the first (in the stack) key to the last door:
hero.command(peasant, "dropItem", {x: 23, y: 35});

// Hurry and collect treasures!
hero.command(peasant, "move", {x: 74, y: 34});
hero.moveXY(10, 35);
hero.jumpTo({x: 15, y: 20});
hero.moveXY(13, 14);
hero.jumpTo({x: 15, y: 57});

```
