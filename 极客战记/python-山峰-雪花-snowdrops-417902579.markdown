---
layout: default
title: snowdrops
---
## 雪花
```

# 我们需要清除陷阱的森林！
# 侦察兵准备了一张森林地图。
#但要注意你拍摄的地方！不要着火。

# 获取森林地图。
forestMap = hero.findNearest(hero.findFriends()).forestMap

# 地图是一个二维数组，其中0是一个陷阱。
# 第一个肯定的镜头。
hero.say("Row " + 0 + " Column " + 1 + " Fire!")

# 但是对于下一点，请在拍摄之前进行检查。
#有一些要检查的点。
cells = [{"row": 0, "col": 4}, {"row": 1, "col": 0}, {"row": 1, "col": 2}, {"row": 1, "col": 4},
    {"row": 2, "col": 1}, {"row": 2, "col": 3}, {"row": 2, "col": 5}, {"row": 3, "col": 0},
    {"row": 3, "col": 2}, {"row": 3, "col": 4}, {"row": 4, "col": 1}, {"row": 4, "col": 2},
    {"row": 4, "col": 3}, {"row": 5, "col": 0}, {"row": 5, "col": 3}, {"row": 5, "col": 5},
    {"row": 6, "col": 1}, {"row": 6, "col": 3}, {"row": 6, "col": 4}, {"row": 7, "col": 0}];

for cell in cells:
    row = cell["row"]
    col = cell["col"]
    # If row is less than forestMap length:
    if row <forestMap.length:
        # If col is less than forestMap[row] length:
        if col<forestMap[row].length:
            # Now, we know the cell exists.
            # If it is 0, say where to shoot:
            if forestMap[row][col]==0:
                hero.say("Row " + row + " Column " + col + " Fire!")

```
