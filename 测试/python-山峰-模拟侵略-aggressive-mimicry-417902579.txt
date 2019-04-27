---
layout: default
title: aggressive-mimicry
---
## 模拟侵略
```

#保护村庄模仿者来了！
#  Ogres把自己伪装成了农民
#检查任何在名字开始时有“Zog”的朋友,攻击
#一定要让真正的农民通过，
#并攻击任何真正的食人魔
#从食人魔保护村庄。
# 注意食人魔，农民和食人魔伪装成“农民”。
#此功能检查文本是否以单词开头。
def startsWith(text, word):
    # If the word is longer then the text:
    if len(word) > len(text):
        return False
    #循环访问单词和文本的索引。
    for index in range(len(word)):
        # 如果具有相同索引的字符不同：
        if word[index] != text[index]:
            # 那么这个词与文本不一致。
            return False
    # 我们检查了所有的信件，它们是一样的。
    return True

ogreNameStart = "Zog"

while True:
    enemy = hero.findNearestEnemy()
    suspect = hero.findNearest(hero.findFriends())
    # 使用函数“startsWith”来检查
    # 如果嫌疑人的姓名（id）以“Zog”开头，则攻击：
    if startsWith(suspect.id, ogreNameStart):
        hero.attack(suspect)
    # 否则，如果有敌人，然后攻击它：
    elif enemy:
        hero.attack(enemy)
    # 否则返回红色的X标记：
    else:
        hero.moveXY(25, 28)

```
