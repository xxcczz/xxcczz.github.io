---
layout: default
title: cluttered-corridors
---
## 杂乱的走廊
```

#帮助宠物找到出口。
#帮助宠物找到满满箱子的杂乱房间的出口。
#听听雕像的提示，
#他们知道路线。
#一个小问题
#他们对信件不满意
#帮助宠物找到出口。

def onHear(event):
    word = event.message
    # 将单词转换为小写。
    word=word.toLowerCase()
    if word == "north":
        pet.moveXY(pet.pos.x, pet.pos.y + 16)
    elif word == "east":
        pet.moveXY(pet.pos.x + 12, pet.pos.y)
    elif word == "south":
        pet.moveXY(pet.pos.x, pet.pos.y - 16)
    elif word == "west":
        pet.moveXY(pet.pos.x - 12, pet.pos.y)

# 为宠物的“听到”事件分配事件处理程序。
pet.on("hear", onHear)

```
