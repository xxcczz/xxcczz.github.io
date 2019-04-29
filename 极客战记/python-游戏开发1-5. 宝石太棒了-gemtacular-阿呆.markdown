---
layout: default
title: gemtacular
---
## 5. 宝石太棒了
```

# Anya在搜索宝石！
# 为关卡添加宝石，以供玩家搜寻。
# 你必须能够通过你的关卡，这样才能继续。

game.spawnHeroXY("captain", 9, 18)
# 使用game.addCollectGoal()来添加宝石收集目标。
game.addCollectGoal()
game.spawnXY("gem", 28, 28)
# 为关卡再添加3个宝石以供玩家收集：
game.spawnXY("gem", 28, 28)
game.spawnXY("gem", 28, 28)
game.spawnXY("gem", 28, 28)

```
