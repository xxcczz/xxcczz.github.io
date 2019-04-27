---
layout: default
title: canyon-of-storms
---
## 山谷的风与牛
```

# 沙漠风暴！收衣服啦！！
# 牛牛检测到风暴迹象

# 把变量做为执行条件
yak = hero.findNearestEnemy()

# 至少还有一只牛牛在场时：
while yak:
    item = hero.findNearestItem()
    if item:
        hero.moveXY(item.pos.x, item.pos.y)
    # 重新给变量赋值
    # with findNearestEnemy()
    yak = hero.findNearestEnemy()
    pass
# 牛没了！
# 快去撤离点：红X
hero.moveXY(38, 58)

```
