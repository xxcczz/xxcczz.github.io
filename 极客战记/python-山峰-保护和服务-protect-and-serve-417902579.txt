---
layout: default
title: protect-and-serve
---
## 保护和服务
```

# Protect the workers and animals!

# Defend these two positions:
defend = []
defend[0] = { "x": 98, "y": 28 }
defend[1] = { "x": 84, "y": 7 }

soldiers = []

friends = hero.findFriends()
for friend in friends:
    if friend.type == "soldier":
        soldiers.append(friend)
    else:
        # Defend the workers:
        defend.append(friend)

while True:
    # Use a for-loop to assign each soldier to a corresponding defend[] target
    # Use command(soldier, "defend", thang) or command(soldier, "defend", position)
    for j in range(len(soldiers)):
        soldier = soldiers[j]
        deff=defend[j]
        hero.command(soldier, "defend", deff)
    pass

```
