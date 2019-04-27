---
layout: default
title: logical-circle
---
## 逻辑圈
```

# 移动到巫师的旁边，获得他的密码
hero.moveXY(20, 24)
secretA = hero.findNearestFriend().getSecretA()
secretB = hero.findNearestFriend().getSecretB()
secretC = hero.findNearestFriend().getSecretC()

# If ALL three values are true, take the high path.
# Otherwise, take the low path. Save the 4th value.
secretD1 = secretA and secretB and secretC
if secretD1:
    hero.moveXY(30, 33)
else:
    hero.moveXY(30, 15)

# If ANY of the three values are true, take the left path.
# Otherwise, go right. Save the 5th value.
secretD2 = secretA or secretB or secretC
if secretD2:
    hero.moveXY(20, 24)
else:
    hero.moveXY(39, 24)

# If ALL five values are true, take the high path.
# Otherwise, take the low path.
secretD3 = secretA and secretB and secretC and secretD1 and secretD2
if secretD3:
    hero.moveXY(30, 33)
else:
    hero.moveXY(30, 15)

```
