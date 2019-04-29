---
layout: default
title: think-ahead
---
## 提前思考
```

#如果你知道敌人的下一步行动，那么你是无懈可击的。
# 你需要分散“大贝莎”，直到你特别的小队到达。
# 大炮射击彼此最接近的一对士兵。

#这个函数找到一对单位
#他们之间的距离最短。
def findNearestPair(units):
    minDistance = 9001
    nearestPair = ["Nobody", "Nobody"]
    # 你需要检查和比较所有的单位。
    # 将索引“i”从0到“len（units）”的所有单元进行迭代。
    for i in range(len(units)):
        #再次使用索引“j”遍历所有单位。
        for j in range(len(units)):
            # 如果“我”等于“j”，则跳过（继续）。
            if j<=i:
                continue
            # 找出第i个和第j个单元之间的距离。
            distance = units[i].distanceTo(units[j])
            #hero.say(distance)
            # 如果距离小于'minDistance'：
            if distance<minDistance:
                #重新分配'minDistance'与新的距离
                minDistance=distance
                nearestPair = [units[i].id, units[j].id]
                # 重新分配'nearestPair'的名字
                #当前对单元的数量。
                
    return nearestPair

```
