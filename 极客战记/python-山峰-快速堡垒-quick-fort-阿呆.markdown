---
layout: default
title: quick-fort
---
## 快速堡垒
```

#遍历所有的工人，让他们建造一座塔。 帐篷。 或围栏
#大声说出农民的名字以及他们的任务，以便他们履行职责
# 我们应该快速建立一个堡垒！
# 每个农民都有一个专业，只能建造一种类型的建筑。
# Carpenter - fences; Mason - towers; builder - tents.
#领班在一个名单中混合他们的名字，但是按照特定的顺序。
#这个清单看起来像[建筑师，泥瓦匠，木匠，建筑师，泥瓦匠，木匠，...]
#使用该列表并为每个农民分配适当的任务。

#工头将工人姓名列表存储为财产。
foreman = hero.findNearest(hero.findFriends())
workerNameList = foreman.workerList


# 使用循环来选择每个第三个元素。
#首先，你需要分配塔的工人。
# 使用起始值1并将索引增加3。
for i in range(1, len(workerNameList), 3):
    # 为他们每个人说出名字和建立内容。
    hero.say(workerNameList[i] + " - tower")

#首先，你需要为帐篷指派工作人员。
#使用起始值0并将索引增加3。
for i in range(0, len(workerNameList), 3):
    # For each of them say to build "tent".
    hero.say(workerNameList[i] + " - tent")

#最后，你需要为篱笆指定工作人员。
# 使用起始值2并将索引增加3。
for i in range(2, len(workerNameList), 3):
    # For each of them say to build "fence".
    hero.say(workerNameList[i] + " - fence")
    
    

# 现在观看战斗或帮助你的军队。

```
