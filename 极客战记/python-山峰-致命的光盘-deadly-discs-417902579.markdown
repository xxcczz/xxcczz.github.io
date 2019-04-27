---
layout: default
title: deadly-discs
---
## 致命的光盘
```

#如果食人魔受到伤害，她会醒来并粉碎农民。
#你可以扔这些剃须刀（）。 也许这会有所帮助？
#看起来你需要三张光碟来击败食人魔。
#让所有三个人同时击中食人魔！
#提示：剃须刀光盘从障碍物反弹！


targets = []
targets.append({ "x": hero.pos.x-5, "y": hero.pos.y  })
targets.append({ "x": hero.pos.x, "y": hero.pos.y + 5 })
targets.append({ "x": hero.pos.x, "y": hero.pos.y - 5 })
#找出丢弃其他两张光碟的位置。
#for a in range(len(targets)):
    #hero.say(a+" "+targets[a].x+targets[a].y)

while len(targets)>0:
    if hero.isReady("throw"):
        # pop(0) 删除并返回数组的第一个元素
        target = targets.pop(0)
        #for a in range(len(targets)):
            #hero.say(a+" "+targets[a].x+targets[a].y)
        hero.throwPos(target)
    else:
        hero.wait(0.01)

```
