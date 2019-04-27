---
layout: default
title: fair-battle
---
## 公平之战
```

# 直到你士兵的总生命值大于兽人的.
# 在你的士兵取得优势前不要发起进攻.

# 编写函数，将单元数组作为输入
# And returns the sum of all the units' health
def jisuanshengmingzhizonghe(jihe):
    sum=0
    for danti in jihe:
        sum=sum+danti.health
    return sum

while True:
    friends = hero.findFriends()
    enemies = hero.findEnemies()
    # 计算并比较你的士兵和兽人的总生命值.
    if jisuanshengmingzhizonghe(friends)>jisuanshengmingzhizonghe(enemies):
        # 当你准备好后说“Attack”.
        hero.say("Attack")

```
