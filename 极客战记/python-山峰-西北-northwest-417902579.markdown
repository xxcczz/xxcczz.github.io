---
layout: default
title: northwest
---
## 西北
```

#你的宠物应该找到，然后把药水带给英雄。

#此功能检查单词是否在文本中。
def wordInText(text, word):
    # 遍历文本中的每个字符。
    for i in range(len(text) - len(word) + 1):
        #为他们每个人循环通过字中的每个字符。
        for j in range(len(word)):
            # Store the shifted index i + j.
            shiftedIndex = i + j
            # 如果移动索引中的字符。
            # 不等于索引“j”中的字中的字符
            if text[shiftedIndex] != word[j]:
                # Break the loop.
                break
            #如果j等于单词中最后一个字母的索引
            if j == len(word) - 1:
                # 那么整个单词就在文本中。
                # 返回True。
                return True
    # 这个词在文本中找不到。返回False。
    return False

# 按照指南的指示在哪里运行
def onHear(event):
    # 如果短语中有“west”，宠物应该向左跑。
    if wordInText(event.message, "west"):
        pet.moveXY(pet.pos.x - 28, pet.pos.y)
    # 如果短语中有“北方”，宠物应该跑起来。
    elif wordInText(event.message, "north"):
        pet.moveXY(pet.pos.x, pet.pos.y + 24)
    # 否则宠物应该尝试拿取药水。
    else:
        potion = pet.findNearestByType("potion")
        if potion:
            pet.fetch(potion)

pet.on("hear", onHear)

```
