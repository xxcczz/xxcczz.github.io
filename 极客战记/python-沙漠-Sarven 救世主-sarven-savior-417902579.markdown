---
layout: default
title: sarven-savior
---
## Sarven 救世主
```

# 一个数组(Array)就是物品的数列。

# 这个数组是一个朋友名字的数列。
friendNames = ['Joan', 'Ronan', 'Nikita', 'Augustus']

# 数组从零开始计数，不是1！
friendIndex = 0

# 循环该数组中的每一个名字
# 使用 len()方法来得到列表的长度。
while friendIndex < len(friendNames):
    # 使用方括号来获得数组中的名字。
    friendName = friendNames[friendIndex]
    
    # 告诉你的朋友回家。
    # 使用+来连接两个字符串。
    hero.say(friendName + ', go home!')
    
    # 增加索引来获取数组中的下一个名字
    friendIndex=friendIndex+1
    
# 回去建造栅栏让食人魔远离。
hero.moveXY(14, 31)
hero.buildXY("fence", 30, 30)

```
