---
layout: default
title: in-my-name
---
## 以我的名义
```

# 你必须出发去找到宝藏.
# 用Thoktar的名字作为线索.
# 正确的宝藏与“z”的索引相同。


#这个函数应该返回一个字母的索引：
def letterIndex(word, letter):
    #逐字通过每个字母作为单词的索引
    for i in range(len(word)):
        #用当前索引存储单词中的一个字符。
        character = word[i]
        # 如果是必填字母：
        if character==letter:
            # 然后返回当前索引（数字）。
            return i
    #如果没有，请返回默认值
    return -1

ogreLetter = "z"
shaman = hero.findByType("thoktar")[0]

#找到索引并用它来寻找宝藏
chestIndex = letterIndex(shaman.id, ogreLetter)
hero.moveXY(16 + chestIndex * 8, 36)

```
