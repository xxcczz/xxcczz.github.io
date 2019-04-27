---
layout: default
title: a-fine-mint
---
## 造币厂
```

# 差役试图偷取金币
# 编写一个函数，在差役盗取金币前将其干掉

def pickUpCoin():
    coin = hero.findNearestItem()
    if coin:
        hero.moveXY(coin.pos.x, coin.pos.y)

# 在下方写一个攻击敌人的函数attackEnemy。
# 寻找最近的敌人，如果出现敌人就进行攻击
def attackEnemy():
    enemy = hero.findNearestEnemy()
    if enemy:
        hero.attack(enemy)

while True:
    attackEnemy() # ∆ 在写好 attackEnemy 函数后消除这里的注释。
    pickUpCoin()

```
