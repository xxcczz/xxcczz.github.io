---
layout: default
title: medic-school
---
## 医学院
```


#那些蘑菇正在燃烧，
#但你需要为军医学生收集10个蘑菇
#你的宠物会帮你拿取魔药，
#但除非医疗名称以“Exp。”开头，否则不要服用魔药
# 收集10个蘑菇。

#此功能检查短语是否以单词开头。
def astartsWith(phrase, word):
    # 如果单词长于文本，则返回False。
    
    #循环访问单词和文本的索引。
    
        # 如果具有相同索引的字符不同：
        
            #返回False。
            
    # 我们检查了所有的信件，它们是一样的。
    #返回True。
    return True
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

def onHear(event):
    # 只接受来自专家的选项。
    if startsWith(event.speaker.id, "Exp"):
        potion = pet.findNearestByType("potion")
        if potion:
            pet.fetch(potion)
            pet.moveXY(28, 34)

pet.on("hear", onHear)
while True:
    mushrooms = hero.findByType("mushroom")
    nearest = hero.findNearest(mushrooms)
    if nearest:
        hero.moveXY(nearest.pos.x, nearest.pos.y)

```
