---
layout: default
title: yeti-away
---
## 离开雪人
```

#从yetis逃脱
#逃离兽医，
#但要小心伏击以“Mac”开头的农民
#从yetis逃脱
#逃离兽医，
#但要小心伏击以“Mac”开头的农民
# 跟随其中一个农民逃离雪人。

def startsWith(phrase, word):
    if len(word) > len(phrase):
        return False
    # 从0到单词长度的迭代索引
    for i in range(len(word)):
        #检查索引i处的短语和单词的字母
        #如果它们不相同：
        if word[i]!=phrase[i]:
            #然后返回False。
            return False
    #检查单词中的所有字母，然后返回true。
    return True

#按照名字以“Mac”开头的当地导游。
guides = hero.findFriends()
for gIndex in range(len(guides)):
    guide = guides[gIndex]
    if startsWith(guide.id, "Mac"):
        while True:
            hero.move(guide.pos)

```
