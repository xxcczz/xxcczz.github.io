---
layout: default
title: storming-the-towers-of-areth
---
## 强攻 Areth 塔
```

# The ogres are holed up in their camp
# Break through their defenses with a calculated strike!

hero.moveXY(55, 14)
hero.moveXY(92, 9)

# 在红色的 X 位置建造一个火焰陷阱
hero.buildXY("fire-trap", 95, 18)
# 撤退到木的 X 位置，来避免伤害。
hero.moveXY(56, 14)
# 等雇佣兵发现闪亮的火焰陷阱
# 进入营地，放置火焰陷阱在红色的 X 位置
hero.buildXY("fire-trap", 89, 52)
hero.buildXY("fire-trap", 60, 61)
# 冲你的部队喊撤退（提示：使用 say 命令, "Retreat!"）
hero.say("Retreat!")
# 逃回到左边的木的 X 位置
hero.moveXY(12, 26)

```
