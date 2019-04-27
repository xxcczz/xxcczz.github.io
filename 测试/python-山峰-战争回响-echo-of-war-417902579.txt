---
layout: default
title: echo-of-war
---
## 战争回响
```

# 摧毁5个机器人炸弹。 其中一些是古老而安全的。
# 旧的（安全）炸弹在他们的身份证上有特定的字母。

# 此功能检查字母是否在单词中。
def isLetterInWord(word, letter):
    # 完成该功能。
    for i in range(len(word)):
        character = word[i]
        if character == letter:
            return True
    return False

# 工程师知道旧机器人是如何标记的。
engineer = hero.findFriends()[0]
safeLetter = engineer.safeLetter

enemies = hero.findEnemies()
for index in range(len(enemies)):
    enemy = enemies[index]
    if isLetterInWord(enemy.id, safeLetter):
        # 在安全的情况下摧毁敌人。
        while enemy.health > 0:
            hero.attack(enemy)

```
