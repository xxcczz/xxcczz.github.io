---
layout: default
title: guard-dog
---
## 看门狗
```

# 你无法帮助农民过河。
# 不过，你的宠物做得到！
# 将你的狼调教成看门狗。

def onSpawn(event):
    while True:
        # 宠物一样可以发现敌人。
        enemy = pet.findNearestEnemy()
        # 如果有敌人：
        if enemy:
            pet.say("message")
            # 然后让宠物说点什么：
            

pet.on("spawn", onSpawn);

```
