---
layout: default
title: square-shield
---
## 方形盾构
```

# Incoming yeti attack!
# Use your paladins to form a square!
# Command Illumina and Vaelia to create a square!

def findByName(name, thangs):
    for i in range(len(thangs)):
        thang = thangs[i]
        if thang.id == name:
            return thang
    return None

friends = hero.findFriends()
celadia = findByName("Celadia", friends)
dedalia = findByName("Dedalia", friends)
sideLength = celadia.distanceTo(dedalia)
bl1=0
points = []
points[0] = {"x": 33, "y": 42}
points[0].x=celadia.pos.x
points[0].y=celadia.pos.y-sideLength
points[1] = {"x": 47, "y": 42}
points[1].x=dedalia.pos.x
points[1].y=dedalia.pos.y-sideLength
for friend in friends:
    if friend.id=="Celadia":
        continue
    if friend.id=="Dedalia":
        continue
    hero.command(friend, "move", points[bl1])
    bl1=bl1+1
# First assign the remaining paladins to variables:

# Command both to move to the corners of the square.
# Remember squares have equal-length sides!

```
