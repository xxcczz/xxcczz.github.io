---
layout: default
title: team-work
---
## 团队合作
```

# Gems will disappear soon. You'll need help!

# findItems() returns an array of items.
items = hero.findItems()

# Get the first gem from the array.
# Don't forget that the first index is 0.
gem0 = items[0]

# # 告诉 Bruno 拿到 gem0
hero.say("Bruno " + gem0)

# You can reference the gem without a variable.
hero.say("Matilda " + items[1])

# Create a variable for the last gem, items[2]:
gem2 =items[2]
# Move to that gem's position using moveXY()
hero.moveXY(gem2.pos.x, gem2.pos.y)

```
