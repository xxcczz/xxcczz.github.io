---
layout: default
title: perimeter-defense
---
## 周界防御
```

#农民必须生存下去
#保护村庄
#用强大的防守建立城镇！
#在村庄周围巡逻，并告诉农民在每个地点建造。
#我们需要在村庄周围建立警戒塔。
#每个农民都可以建一座塔。
#向他们展示建造的地方。
#这些塔是自动的，会攻击城外的所有单位。

# 首先沿着北边界（y = 60）从x = 40移动到x = 80，随着步骤20。
# 范围不包括第二个边缘。
for x in range(40, 81, 20):
    #在每个点上移动并说出任何内容。
    hero.moveXY(x, 60)
    hero.say("Here")
    
# 接下来沿着东边界（x = 80）从y = 40移动到y = 20，以负的步长-20移动。对于范围内的y（40,19,20）：

for y in range(40, 19, -20):
    hero.moveXY(80, y)
    hero.say("Here")
# 继续其余两个边界。
# 接下来是南边界（y = 20），从x = 60到x = 20，负-20步。
for x in range(60, 19, -20):
    hero.moveXY(x, 20)
    hero.say("Here")
# 接下来是步骤20，从y = 40到y = 60的西边界（x = 20）。
for y in range(40, 61, 20):
    hero.moveXY(20, y)
    hero.say("Here")
# 不要忘记躲在村里。
hero.moveXY(50, 40)

```
