---
layout: default
title: loud-quietness
---
## 吵闹  宁静
```

#你的英雄必须到达房间的尽头
#你的宠物必须到达房间的尽头
#帮助英雄和宠物走出房间
#士兵有密码和音量属性
#使用字符串方法tolower case（）和touppercase（）来使用所需的情况
#将英雄和他们的宠物移到出口处。

def onHear(event):
    # 获取音量和密码。
    #hero.say(event.message)
    words = event.message.split(" ")
    volume = words[0]
    password = words[1]
    #如果密码应该很大：
    if volume == "Loud":
        #宠物用大写字母重复它。
        pet.say(words[1].toUpperCase())
    # 如果密码应该是安静的：
    if volume == "Quiet":
        # 宠物以小写字母重复。
        pet.say(words[1].toLowerCase())
    pet.moveXY(pet.pos.x+ 24, pet.pos.y)

def passDoor():
    guard = hero.findNearest(hero.findFriends())
    password = guard.password
    # 如果密码应该很大：
    if guard.isLoud:
        #在密码上使用.toUpperCase（）方法。
        hero.say(password.toUpperCase())
        pass
    #如果密码应该是安静的：
    elif guard.isQuiet:
        # 在密码上使用.toLowerCase（）方法。
        hero.say(password.toLowerCase())
        pass
    hero.moveXY(hero.pos.x+ 24, hero.pos.y)

# 让宠物听到警卫
pet.on("hear", onHear)
#英雄通过门的代码。
hero.moveXY(10, 14)
passDoor()
passDoor()

```
