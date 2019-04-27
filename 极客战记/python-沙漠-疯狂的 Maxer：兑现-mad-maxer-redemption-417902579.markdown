---
layout: default
title: mad-maxer-redemption
---
## 疯狂的 Maxer：兑现
```

# 你不能到你朋友那边去保卫他们！
# 告诉他们回家，弓箭手会帮助他们

while True:
    weakestFriend = None
    leastHealth = 9999
    friendIndex = 1
    # Find which friend has the lowest health.
    friends = hero.findFriends()
    while friendIndex<len(friends):
        friend=friends[friendIndex]
        if friend.health<leastHealth:
            leastHealth=friend.health
            weakestFriend=friend
        friendIndex=friendIndex+1
    # 告诉最弱的朋友先回家。
    if weakestFriend:
        hero.say('Hey ' + weakestFriend.id + ', go home!')

```
