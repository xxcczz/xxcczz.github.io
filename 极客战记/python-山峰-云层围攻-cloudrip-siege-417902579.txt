---
layout: default
title: cloudrip-siege
---
## 云层围攻
```

#你的目标是保持至少一朵鲜花持续60秒。    
#这是一个可选的挑战级别，意图很难。 用你的代码创意！    
#每次成功时，它变得越来越难（而且更赚钱）。 如果你失败了，你必须等待一天才能重新提交。    
a=1    
while True:    
    if hero.gold >= hero.costOf("arrow-tower"):    
        if a==1:    
            hero.buildXY("arrow-tower", 75, 42)    
            a=0    
        else:    
            hero.buildXY("arrow-tower", 20, 42)    
            a=1    
    js()    
    jianjinbi()    
def js():    
    if hero.canCast("haste", hero):    
        hero.cast("haste", hero)    
    else:    
        cooldown = hero.getCooldown("haste")
        if cooldown!=0:
            hero.resetCooldown("haste")
    
def jianjinbi():    
    items = hero.findItems()    
    a=None    
    maxjz=0    
    for item in items:    
        jz=item.value/hero.distanceTo(item)    
        if jz>maxjz:    
            maxjz=jz    
            a=item    
    if a:    
        hero.move(a.pos)   
    
```
