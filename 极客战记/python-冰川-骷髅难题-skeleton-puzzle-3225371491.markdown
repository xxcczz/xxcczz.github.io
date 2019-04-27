﻿---
layout: default
title: skeleton-puzzle
---
## 骷髅难题
```

def moveTo():
    if (currentY > 0):
        if check(currentY, currentX, currentY - 1, currentX):
            return True
    if (currentX < 2):
        if check(currentY, currentX, currentY, currentX + 1):
            return True
    if (currentY < 2):
        if check(currentY, currentX, currentY + 1, currentX):
            return True
    if (currentX > 0):
        if check(currentY, currentX, currentY, currentX - 1):
            return True


def check(yt, xt, yf, xf):
    goal = getLastCoors(yf, xf)
    if (yf > yt and yf > goal.y):
        hero.say(puzzleState[yf][xf])
        return True
    if (yf < yt and yf < goal.y):
        hero.say(puzzleState[yf][xf])
        return True
    if (xf < xt and xf < goal.x):
        hero.say(puzzleState[yf][xf])
        return True
    if (xf > xt and xf > goal.x):
        hero.say(puzzleState[yf][xf])
        return True
    return False


def getLastCoors(yf, xf):
    num = puzzleState[yf][xf]
    for y in range(0, 3):
        for x in range(0, 3):
            if goalState[y][x] == num:
                xg = x
                yg = y
    return {'x': xg, 'y': yg}

# The necromancer always knows the puzzle state.
boneMaster = hero.findFriends()[0]
puzzleState = boneMaster.getPuzzleState()
# The result state should be this:
goalState = [[1, 2, 3], [4, 5, 6], [7, 8, 0]]

# Solve, Solve, Solve!
currentX = 0
currentY = 0
count = 0;
while True:
    puzzleState = boneMaster.getPuzzleState()
    count = 0
    for y in range(0, 3):
        for x in range(0, 3):
            if puzzleState[y][x] == goalState[y][x]:
                count = count + 1
            if puzzleState[y][x] == 0:
                currentX = x
                currentY = y
    if count > 7:
        break
    else:
        
        moveTo()

```
