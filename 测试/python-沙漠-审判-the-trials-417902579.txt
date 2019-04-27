---
layout: default
title: the-trials
---
## 审判
```

# 本关是专为高级玩家准备的。解决方案应该是非常的复杂的，使用了大量的招数。它可能是一种类似齿轮检查的精细活，除非你使用“创造性”的方法。
# 你需要到第一个审判的地点（玛尔绿洲），杀死前进的道路上的敌人。当你达到那里，捡走所有的蘑菇触发的审判开始。如果你在冲击活下来，你会进入下一个绿洲进行第二次审判，然后是寺庙。当所有的审判都完成后你将不得不面对最终BOSS。祝你好运！
# 提示：在本关具有高可见范围的眼镜会有极大的帮助，所以尽可能的买好的眼镜吧。
# 提示：绿洲守卫单位的类型是「oasis-guardian」
while True:
    flag = hero.findFlag()
    enemy = hero.findNearestEnemy()
    friend = hero.findFriends()[0]
    item = hero.findNearestItem()
    if flag:
        hero.pickUpFlag(flag)
    elif enemy:
        hero.attack(enemy)
    elif friend:
        hero.attack(friend)
    elif item:
        yidong(item)
    
        
    

def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

```
