---
layout: default
title: twins-power
---
## 孪生力量
```

#有四对双胞胎，他们应该成对地祈祷。
#你需要找到双胞胎并给他们打电话。
def onSpawn (event):
    while True:
        enemy = pet.findNearestEnemy()
        if enemy:
            pet.say(enemy.health)

pet.on("spawn", onSpawn)

# 双胞胎有相同的名字，只有最后一个字母是不同的。
# 此功能检查一对单位是否是双胞胎。
def areTwins(unit1, unit2):
    name1 = unit1.id
    name2 = unit2.id
    if name1.length != name2.length:
        return False
    for i in range(name1.length - 1):
        if name1[i] != name2[i]:
            return False
    return True

#遍历所有的圣骑士和圣骑士
#如果他们是双胞胎，则说他们的名字是成对的。

friends = hero.findFriends()
for i in range(len(friends)):
    for j in range(len(friends)):
        if j<=i:
            continue
        if areTwins(friends[i], friends[j]):
            hero.say(friends[i].id+" "+friends[j].id)



# 例如：hero.say（“NameTwin1 NameTwin2”）

# 当双胞胎在他们的位置时，引诱食人魔。
#不要怕梁 - 它们只对食人魔是危险的。
while True:
    if hero.time>6:
        flag = hero.findFlag()
        if flag:
            hero.pickUpFlag(flag)
        else:
            hero.shield()
            #ml()
def ml():
    friends = hero.findFriends()
    for friend in friends:
        enemy=friend.findNearestEnemy()
        if enemy and enemy.pos.x<57:
            hero.command(friend, "attack", enemy)


```
