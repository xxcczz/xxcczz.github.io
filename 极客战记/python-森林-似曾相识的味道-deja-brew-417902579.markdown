---
layout: default
title: deja-brew
---
## 似曾相识的味道
```

# 你可以把字符串连起来，或者把数字连接到字符串中。
# Sing along, using string concatenation:
# X potions of health on the wall!
# X potions of health!
# Take Y down, pass it around!
# X-Y potions of health on the wall.

potionsOnTheWall = 10
numToTakeDown = 1
while True:
    hero.say(potionsOnTheWall + " potions of health on the wall!")
    # 唱出下一句：
    hero.say(potionsOnTheWall + " potions of health!")
    # 唱出下一句：
    hero.say("Take "+numToTakeDown+" down, pass it around!")
    potionsOnTheWall -= numToTakeDown
    # 唱出最后一句：
    hero.say(potionsOnTheWall + " potions of health on the wall!")

```
