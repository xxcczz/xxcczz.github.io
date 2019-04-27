---
layout: default
title: flawless-pairs
---
## 无暇的宝石对
```

#为了逃离墓地，你需要找到四对相同的宝石。
#收集4双宝石。
#每一对必须包含相同的宝石。

# 此函数返回两个具有相同值的项目。
def findValuePair(items):
    # 检查数组中的每个可能的对。
    # 从0到最后一个迭代索引'i'。
    for i in range(len(items)):
        itemI = items[i];
        # 从0到最后遍历索引'j'。
        for j in range(len(items)):
            #如果它是相同的元素，则跳过它。
            if j<=i:
                continue
            itemJ = items[j];
            #如果我们发现一对有两个相同的宝石，然后返回它们。
            if itemI.value == itemJ.value:
                return [itemI, itemJ]
    # 如果没有配对，则返回一个空数组。
    return None


while True:
    gems = hero.findItems()
    gemPair = findValuePair(gems)
    # 如果gemPair存在，收集宝石！
    if gemPair:
        gemA = gemPair[0]
        gemB = gemPair[1]
        #移至第一个宝石。
        hero.moveXY(gemA.pos.x, gemA.pos.y)
        #回归让巫师加速。
        hero.moveXY(40, 43)
        # 然后移动到第二个宝石。
        hero.moveXY(gemB.pos.x, gemB.pos.y)
        # 回归让巫师加速。
        hero.moveXY(40, 43)
        pass

```
