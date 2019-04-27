---
layout: default
title: grid-search
---
## 网格搜索
```

#树之间的宝藏。
# 坐标是'x：？0，y：？0'。
# 移动所有可能的点并向农民展示挖掘的地方。

leftBorder = 20
rightBorder = 61
bottomBorder = 20
topBorder = 51
step = 10

# 从左到右循环X坐标与第10步的边界。
for x in range(leftBorder, rightBorder, step):
    # 使用嵌套循环遍历每个X的Y坐标。
    # 从步骤10的底部到顶部边界迭代y坐标。
    for y in range(bottomBorder, topBorder, step):
        # 移动到坐标为X，Y的点并说出任何内容。
        hero.moveXY(x, y)
        hero.say("message")
    pass

# 让农民检查最后一点。
hero.moveXY(20, 10)

```
