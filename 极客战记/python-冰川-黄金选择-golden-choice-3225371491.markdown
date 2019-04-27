﻿---
layout: default
title: golden-choice
---
## 黄金选择
```

distanceX = 4
distanceY = 6
zeroPoint = {"x": 14, "y": 14}
lines = 10

goldMap = [[0 for j in range(2 * lines - 1)] for i in range(lines)]
for coin in hero.findItems():
    row = int((coin.pos.y - zeroPoint.y) / distanceY)
    col = int((coin.pos.x - zeroPoint.x) / distanceX)
    goldMap[row][col] = coin.value

map = reversed(goldMap)
rows = len(map)
cols = len(map[0])

for r in range(1, rows):
    map[r - 1] += [0]
    for c in range(cols):
        if map[r][c] == 0:
            continue
        # map[r][c] += max(map[r-1][c-1], map[r-1][c+1])

        if c == 0:
            map[r][c] += map[r - 1][c + 1]
        elif c == cols - 1:
            map[r][c] += map[r - 1][c - 1]
        else:
            map[r][c] += max(map[r - 1][c - 1], map[r - 1][c + 1])

map = reversed(map)

for r in range(rows):
    if r == 0:
        c = map[r].index(max(map[r]))
        hero.moveXY(c * distanceX + 14, 7)
    else:
        if map[r][c + 1] > map[r][c - 1]:
            c += 1
        else:
            c -= 1
            #    hero.say("Next: " + str(c * distanceX + 14) + ", " + str(r * distanceY + 14))
    hero.moveXY(c * distanceX + 14, r * distanceY + 14)

```
