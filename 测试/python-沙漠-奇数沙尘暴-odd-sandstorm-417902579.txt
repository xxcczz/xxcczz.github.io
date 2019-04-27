---
layout: default
title: odd-sandstorm
---
## 奇数沙尘暴
```

# 这个数组包含朋友和食人魔。
# 偶数元素是食人魔，奇数元素是伙伴。
everybody = ['Yetu', 'Tabitha', 'Rasha', 'Max', 'Yazul',  'Todd']
enemyIndex = 0

while enemyIndex < len(everybody):
    # 使用方括号把食人魔的名字从数组中获取出来
    a = everybody[enemyIndex]
    # 使用变量传入食人魔的名字，攻击它们。
    hero.attack(a)
    # 每次递增2，来跳过朋友。
    enemyIndex += 2

# 在击败食人魔之后，向绿洲移动。
hero.moveXY(36,52)

```
