---
layout: default
title: reindeer-wakeup
---
## 驯鹿苏醒
```

#通过使用数组来追踪他们，帮助盲人牧民唤醒他的驯鹿。
# 这个数组包含每个驯鹿的状态。
deerStatus = [ 'asleep', 'asleep', 'asleep', 'asleep', 'asleep' ]

#这个数组包含我们的驯鹿。
friends = hero.findFriends()

#循环驯鹿并找到清醒的人：
for deerIndex in range(len(friends)):
    reindeer = friends[deerIndex]
    
    # y位置> 30的驯鹿不在笔中。
    #如果是这样，请将驯鹿的条目设置为“清醒”。
    if reindeer.pos.y>30:
        deerStatus[deerIndex]="awake"
    pass

#通过状态循环并向Merek报告。
for statusIndex in range(len(deerStatus)):
    # 告诉梅里克驯鹿指数及其状态。
    # 说一些像“驯鹿2睡着了”。"Reindeer 2 is asleep".
    hero.say("Reindeer "+statusIndex+" is "+deerStatus[statusIndex])
    pass

```
