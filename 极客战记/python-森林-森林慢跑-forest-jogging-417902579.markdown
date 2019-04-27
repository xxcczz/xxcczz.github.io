---
layout: default
title: forest-jogging
---
## 森林慢跑
```

# 你的宠物可以使用 pet.moveXY()

def onSpawn(event):
    while True:
        # 首先，移动到左侧X标记处：
        pet.moveXY(9, 24)
        # 接着，移动到上面的X标记。
        pet.moveXY(30, 43)
        # 将宠物移动至右侧的X标记处：
        pet.moveXY(51, 24)
        # 将你的宠物移动到下面的X标记处：
        pet.moveXY(30, 5)
pet.on("spawn", onSpawn)

# 使用pet.on()，通过onSpawn来处理"spawn"事件


# 激励你的宠物！
# 不要移除下方的命令。
while True:
    hero.say("狗狗真棒！")
    hero.say("你能做到的！")
    hero.say("跑跑跑！")
    hero.say("快好了！")
    hero.say("再来一圈！")

```
