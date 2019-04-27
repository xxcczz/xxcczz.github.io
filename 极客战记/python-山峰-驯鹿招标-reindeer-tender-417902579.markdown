---
layout: default
title: reindeer-tender
---
## 驯鹿招标
```

# 数组(5个叉叉)
penPositions = [ {"x":20,"y":24}, {"x":28,"y":24}, {"x":36,"y":24}, {"x":44,"y":24}, {"x":52,"y":24} ]

# 使用这个数组来知道每个叉叉有没有驯鹿
penOccupants = [ None, None, None, None, None, ]

# 这个数组包含我们的驯鹿
friends = hero.findFriends()

# 找出哪些驯鹿已经在他们的笔中,遍历驯鹿
for deerIndex in range(len(friends)):
    reindeer = friends[deerIndex]
    
    # 遍历每个位置检查是否有驯鹿。
    for penIndex in range(len(penPositions)):
        penPos = penPositions[penIndex]
        
        if penPos.x == reindeer.pos.x and penPos.y == reindeer.pos.y:
            #把驯鹿放在占有者的penIndex处
            penOccupants[penIndex]=1
            # 从朋友阵列中删除驯鹿。
            friends[deerIndex]=None
            # 在这里跳出内部循环：
            break
            pass
#可以检查一下统计的结果,10100
#b=0
#for a in penOccupants:
#    if a==None:
#        hero.say(b+":"+0)
#    else:
#        hero.say(b+":"+a)
#    b=b+1
#将剩下的驯鹿分配到新位置。
for deerIndex in range(len(friends)):
    #如果驯鹿为空，请使用continue
    reindeer = friends[deerIndex]
    if reindeer==None:
        continue
    # 寻找没有任何东西的第一个位置
    for occIndex in range(len(penOccupants)):
        # 如果什么也没有，说明这个位置没有驯鹿
        if penOccupants[occIndex]==None:
            # 命令驯鹿走到空位置去
            hero.command(reindeer, "move", penPositions[occIndex])
            penOccupants[occIndex]=1
            break
            pass

```
