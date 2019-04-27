---
layout: default
title: cannon-landing-force
---
## 大炮陆战队
```

#我们应该派士兵去保卫村庄。
#我们还需要清除旧的陷阱。
#对于这两个目标，我们将使用炮兵！
#炮兵可以发射士兵和反陷阱。

#侦察兵准备了着陆区的地图。
#地图是单元格是字符串的二维数组。
landingMap = hero.findNearest(hero.findFriends()).landingMap

# 告诉大炮行，列和目标类型。
#要获取元素，请使用array [i] [j]
# 首先，让我们看看第0行和第0列。
cell = landingMap[0][0]
#接下来，说出坐标和有什么。
hero.say("row 0 column 0 " + cell)

# 下一个单元格是第3行和第2列。
hero.say("row 3 column 2 " + landingMap[3][2])

#现在自己做下一点：
#第2行和第1列。
hero.say("row 2 column 1 " + landingMap[2][1])
#第1行和第0列。
hero.say("row 1 column 0 " + landingMap[1][0])
#第0行和第2列。
hero.say("row 0 column 2 " + landingMap[0][2])
#第1行和第3列。
hero.say("row 1 column 3 " + landingMap[1][3])

```
