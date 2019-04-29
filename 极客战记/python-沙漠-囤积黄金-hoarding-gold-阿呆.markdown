---
layout: default
title: hoarding-gold
---
## 囤积黄金
```

# 收集25金币，然后告诉 Naria 总数
# 当金币总数大于25，使用 break 来停止收集金币。

totalGold = 0
while True:
    coin = hero.findNearestItem()
    if coin:
        # 捡起金币
        hero.moveXY(coin.pos.x, coin.pos.y)
        # 将金币的价值加进 totalGold.(查看帮助了解更多.)
        # 使用以下方法得到它的价值：:  coin.value
        totalGold=totalGold+coin.value
        pass
    if totalGold >= 25:
        # 这会中断循环并且执行循环下面的语句
        # The loop ends, code after the loop will run.
        break



# 完成收集金币！
hero.moveXY(58, 33)
# 去告诉 Naria 你收集了多少金币。
hero.say(totalGold)

```
