---
layout: default
title: danger-valley
---
## 危险谷
```

#远离食人魔的视线
#用陷阱击败所有食人魔
#设立一片地雷来吸引食人魔！
#答案在于一组嵌套数组，因此请仔细布置防火墙
# Ogres把一些农民劫为人质！
# 侦察员给你一个伏击的英雄。
# this.grid包含一个数组数组。
# 在子数组中，0是农民，1是食人魔。
# 使用这些信息来设置陷阱。

#记住包含数组只是一个数组！
# 遍历这个数组的所有元素。
for i in range(len(hero.grid)):
    row = hero.grid[i]
    #现在，行只是另一个数组！
    # 遍历此数组中的所有切片：
    for j in range(len(row)):
        #检查i，j的tile是否为1：
        #hero.buildXY("fire-trap", 36 + 6 * j, 20 + 6 * i)
        tile = hero.grid[i][j]
        if tile ==1:
            hero.buildXY("fire-trap", 36 + 6 * j, 20 + 6 * i)
#最后，撤回掩护。
hero.moveXY(28, 56)

```
