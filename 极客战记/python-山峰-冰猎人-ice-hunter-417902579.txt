---
layout: default
title: ice-hunter
---
## 冰猎人
```

# 寻找4只牦牛。只选择小的。
# 小牦牛名称包含一个“bos”子字符串。

#这个函数检查一个单词是否包含一个子串。
def isSubstring(word, substring):
    # 我们只遍历开始索引。
    #hero.say(word+","+substring)
    rightEdge = len(word) - len(substring)
    # 循环访问单词的索引。
    for i in range(rightEdge + 1):
        # 对于它们中的每一个循环遍历子字符串
        for j in range(len(substring)):
            #为单词的索引使用偏移量。
            shiftedIndex = i + j
            #如果字母不一样：
            if word[shiftedIndex] != substring[j]:
                # 检查单词中的下一个起始索引。
                break
            #如果它是子字符串中的最后一个字母：
            if j == len(substring) - 1:
                # 然后子字符串在单词中。
                return True
    # 我们还没有找到这个词的子串。
    return False

#循环所有敌人。
enemies = hero.findEnemies()
for e  in range(len(enemies)):
    enemy = enemies[e]
    #使用函数isSubstring来检查
    #如果敌方名称（id）包含“bos”：
    if isSubstring(enemy.id, "bos"):
        # 然后击败它。
        hero.attack(enemy)

```
