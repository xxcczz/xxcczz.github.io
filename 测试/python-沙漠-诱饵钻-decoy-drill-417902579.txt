---
layout: default
title: decoy-drill
---
## 诱饵钻
```

# 我们在测试一个新的战斗单位：诱饵。
# 创建4个诱饵，然后汇报给 Naria
def yidong(mb):
    hero.moveXY(mb.pos.x, mb.pos.y)

decoysBuilt = 0
while True:
    coin = hero.findNearestItem()
    
    if coin:
        # 掠夺金币！
        yidong(coin)
        pass
    # 每个诱饵消费25个金币。
    # 让它知道当你有超过25个金币的时候
    if hero.gold>25:
        hero.buildXY("decoy", hero.pos.x, hero.pos.y)
        # buildXY a "decoy"
        decoysBuilt=decoysBuilt+1
        # 当你一直走的时候，保持统计你创建的诱饵的数量。
        
    if decoysBuilt == 4:
        # 当你创建了4个诱饵时跳出循环
        break
        pass
    
hero.say("完成创建诱饵！")
hero.moveXY(14, 36)
# 去找 Naria 并告诉她你创建了多少个诱饵。
hero.say(decoysBuilt)

```
