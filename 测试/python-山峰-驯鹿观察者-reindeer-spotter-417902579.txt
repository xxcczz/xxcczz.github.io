---
layout: default
title: reindeer-spotter
---
## 驯鹿观察者
```

#通过检查数组帮助盲人牧民将驯鹿放入他们的笔中。
#这个数组包含每个笔的位置。
penPositions = [ {'x':20,'y':24}, {'x':28,'y':24}, {'x':36,'y':24}, {'x':44,'y':24}, {'x':52,'y':24} ]

#这个数组用来跟踪哪个驯鹿在里面。
penOccupants = [ 'empty', 'empty', 'empty', 'empty', 'empty' ]

#这个数组包含我们的驯鹿。
friends = hero.findFriends()

#找出哪些驯鹿已经在他们的笔中。
for deerIndex in range(len(friends)):
    reindeer = friends[deerIndex]
    
    #检查每支笔是否符合驯鹿的位置。
    for penIndex in range(len(penPositions)):
        penPos = penPositions[penIndex]
        
        if penPos.x == reindeer.pos.x and penPos.y == reindeer.pos.y:
            #把penOccupants中的id放在penIndex处。
            penOccupants[penIndex]="Dasher"
            #在这里突破内部循环。
            
            pass

# 告诉Merek每支笔里有什么。
for occIndex in range(len(penOccupants)):
    # 告诉Merek笔指数和占有者。
    # 说一些像"Pen 3 is Dasher"
    hero.say("Pen "+occIndex+" is "+penOccupants[occIndex])
    pass

```
