---
layout: default
title: bash-em-all
---
## 猛砸他们全家
```

# 小心那些食人魔。
# 它们是特殊训练的低脂肪超强食人魔。
# 关键词是“低脂肪”
cishu=0
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.bash(enemy)
        #cishu=cishu+1
        #hero.say(cishu)
        hero.moveXY(40, 33)
    else:
        item = hero.findNearestItem()
        if item:
            yidong(item)
            hero.moveXY(40, 33)

    
    

def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
