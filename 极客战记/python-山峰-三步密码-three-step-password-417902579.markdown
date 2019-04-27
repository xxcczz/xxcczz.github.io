---
layout: default
title: three-step-password
---
## 三步密码
```

#找到大门的密码并击败食人魔。

#获取秘密消息
hero.moveXY(52, 50)
friend = hero.findNearest(hero.findFriends())
message = friend.message

# 获取分隔符。
hero.moveXY(66, 34)
friend = hero.findNearest(hero.findFriends())
separator = friend.separator

#获取索引。
hero.moveXY(52, 18)
friend = hero.findNearest(hero.findFriends())
index = friend.index

#走向大门
hero.moveXY(44, 34)
#用分隔符分割消息以获取数组：
messages = message.split(separator)
#通过索引从单词数组中获取密码：
word=messages[index]
#说出密码：
hero.say(word)

# 击败食人魔：
while True:
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

```
