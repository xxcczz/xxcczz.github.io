---
layout: default
title: vision-of-ogres
---
## 食人魔幻象
```

#击败食人魔。
#每波中只有一个食人魔是真实的。
#摧毁他人，其他人将会堕落。
#你可以通过名字识别真正的食人魔。
#每个人都有三个名字。
#Thereal食人魔有一个中间名，以相同的字母开头和结尾（ca#seirrelevant）。
#不要忘记使用小写函数来避免大小写比较问题P S：不要破坏镜像，碎片是尖锐的
# 摧毁一个真正的食人魔，幻想会消失。

def findRealEnemy(enemies):
    for index in range(len(enemies)):
        enemy = enemies[index]
        # 将敌人的名字（id）转换为小写
        # 并将其保存在一个变量中。
        #hero.say(enemy.id)
        word=enemy.id.toLowerCase()
        #hero.say(word)
        # 用空格分隔名称并保存单词。
        words = word.split(" ")
        # 将第二个单词存储在一个变量中。
        w2=words[1]
        #hero.say(w2)
        # 如果第二个字的第一个字母等于
        #这个词的最后一个字母。
        if w2[0]==w2[len(w2)-1]:
            # 那真的是真的。 返回敌人。
            return enemy
#只能攻击真正的食人魔。
while True:
    ogres = hero.findEnemies()
    realOgre = findRealEnemy(ogres)
    if realOgre:
        while realOgre.health > 0:
            hero.attack(realOgre)

```
