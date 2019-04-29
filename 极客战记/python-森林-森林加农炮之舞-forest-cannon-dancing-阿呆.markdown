---
layout: default
title: forest-cannon-dancing
---
## 森林加农炮之舞
```

# 你的宠物应该在X标记上来回跑动
# 英雄需要时刻保持兴奋！

# 为宠物编写事件函数onSpawn
# 这个函数要让狼来回跑动：
# 首先，跑到右侧的标记上，然后左侧的标记：
def onSpawn(event):
    while True:
        pet.moveXY(48, 8)
        pet.moveXY(12, 8)

    


pet.on("spawn", onSpawn)
# 鼓舞你的宠物。不要移除这个：
while True:
    hero.say("跑！！！")
    hero.say("速度！")

```
