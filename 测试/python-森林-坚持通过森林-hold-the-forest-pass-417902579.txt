---
layout: default
title: hold-the-forest-pass
---
## 坚持通过森林
```

# 使用旗子加入战斗或者撤退。
# 如果你失败了，再次点击 提交 生成新的随机敌人，再来一次！
# You'll want at least 300 health, if not more.
while True:
    enemy = hero.findNearestEnemy()
    flag = hero.findFlag()
    if flag:
        # 捡起旗子。
        hero.pickUpFlag(flag)
        pass
    elif enemy:
        # 开打！
        hero.attack(enemy)
        pass

```
