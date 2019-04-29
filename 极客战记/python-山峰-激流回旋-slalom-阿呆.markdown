---
layout: default
title: slalom
---
## 激流回旋
```

# 使用对象枚举来走安全的路，并收集宝石。    
# 在本关你不能够使用 moveXY()方法！使用 move()来移动    
gems = hero.findItems()    
jb=0    
x=20    
y=25    
bh=0    
#hero.say(x+bh*10)    
while hero.pos.x < x+bh*10:    
    # move()移动物体通过 x 和 y 的属性，不仅仅是数字。
    hero.move({'x': x+bh*10, 'y': 35})
#hero.say("...")    
#hero.say(y+bh*10)    
while hero.pos.x < y+bh*10:    
    # 一个宝石的位置是一个对象，有 x 和 y 属性。
    gem0 = gems[bh]
    hero.move(gem0.pos)
    if hero.gold>jb:
        jb=hero.gold
        break
bh=bh+1    
# 当你的 x 小于30的时候，    
# 使用物体移动到30，35位置    
#hero.say(x+bh*10)    
while hero.pos.x < x+bh*10:    
    # move()移动物体通过 x 和 y 的属性，不仅仅是数字。
    hero.move({'x': x+bh*10, 'y': 35})
#hero.say("...")    
#hero.say(y+bh*10)    
while hero.pos.x < y+bh*10:    
    # 一个宝石的位置是一个对象，有 x 和 y 属性。
    gem0 = gems[bh]
    hero.move(gem0.pos)
    if hero.gold>jb:
        jb=hero.gold
        break
bh=bh+1    
# 当你的 x 小于35的时候    
# 移动到宝石[1]的位置    
#hero.say(x+bh*10)    
while hero.pos.x < x+bh*10:    
    # move()移动物体通过 x 和 y 的属性，不仅仅是数字。
    hero.move({'x': x+bh*10, 'y': 35})
#hero.say("...")    
#hero.say(y+bh*10)    
while hero.pos.x < y+bh*10:    
    # 一个宝石的位置是一个对象，有 x 和 y 属性。
    gem0 = gems[bh]
    hero.move(gem0.pos)
    if hero.gold>jb:
        jb=hero.gold
        break
bh=bh+1    
# 拿到最后一对宝石！    
#hero.say(x+bh*10)    
while hero.pos.x < x+bh*10:    
    # move()移动物体通过 x 和 y 的属性，不仅仅是数字。
    hero.move({'x': x+bh*10, 'y': 35})
#hero.say("...")    
#hero.say(y+bh*10)    
while hero.pos.x < y+bh*10:    
    # 一个宝石的位置是一个对象，有 x 和 y 属性。
    gem0 = gems[bh]
    hero.move(gem0.pos)
    if hero.gold>jb:
        jb=hero.gold
        break
bh=bh+1   

```
