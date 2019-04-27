---
layout: default
title: toil-and-trouble
---
## 劳心劳力
```

# 食人魔巫师为您准备了一坨惊喜。

# 定义一个 chooseTarget 函数，让它接受friend 参数输入
# 返回要攻击的目标，根据士兵的类型。
# 士兵应该攻击巫师，弓箭手应该攻击最近的敌人。
def chooseTarget(friend):
    if friend.type=="soldier":
            defendPos = {"x": 41, "y": 40}
            defendPos.x=friend.pos.x+10
            defendPos.y=friend.pos.y
            hero.command(friend, "defend", defendPos)
    if friend.type=="archer":
        enemy = friend.findNearestEnemy()
        hero.command(friend, "attack", enemy)

while True:
    friends = hero.findFriends()
    for friend in friends:
        # 用你的 chooseTarget 函数决定要攻击什么。
        chooseTarget(friend)

```
