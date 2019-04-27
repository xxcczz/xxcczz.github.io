---
layout: default
title: alpine-rally
---
## 高山拉力
```

# 逃离右边的地图    
# 为了逃脱的雪人，你必须让自己更快。    
# 使用resetCooldown来施法更频繁    
# manaBlast能帮我们清理道路    
while True:    
    if hero.canCast("haste", hero):    
        hero.cast("haste", hero)    
    else:    
        cooldown = hero.getCooldown("haste")
        if cooldown!=0:
            hero.resetCooldown("haste")
    hero.move({'x': hero.pos.x+100, 'y': hero.pos.y})    
    if hero.pos.x>107:    
        hero.manaBlast()   

```
