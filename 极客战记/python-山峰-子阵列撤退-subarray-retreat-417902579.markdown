---
layout: default
title: subarray-retreat
---
## 子阵列撤退
```

#找到具有最佳总结价值的宝石子阵列。
# 此功能可以在线性时间内解决问题。
def dynamicMaxSum (gems):
    cycles = 0
    maxStartIndex = 0
    maxEndIndex = 0
    maxEndHere = gems[0].value
    currentStartIndex = 0
    maxBest = 0
    for i in range(len(gems)):
        cycles += 1
        maxEndHere += gems[i].value
        if maxEndHere < 0:
            maxEndHere = 0
            currentStartIndex = i + 1
        if maxEndHere > maxBest:
            maxStartIndex = currentStartIndex
            maxEndIndex = i
            maxBest = maxEndHere
    hero.say("I's taken " + cycles + " cycles.")
    return [maxStartIndex, maxEndIndex]
# 此功能以二次方式解决问题。
def naiveMaxSum(gems):
    cycles = 0
    maxStartIndex = 0
    maxEndIndex = 0
    maxBest = 0
    for i in range(len(gems)):
        sum = 0
        for j in range(i, len(gems)):
            cycles += 1
            if cycles > 104:
                hero.say("我厌倦了计算.")
                return [i, j]
            sum += gems[j].value
            if sum > maxBest:
                maxStartIndex = i
                m = j
                maxBest = sum
    hero.say("I's taken " + cycles + " cycles.")
    return [maxStartIndex, maxEndIndex]
# 不要担心“findItems”通过X坐标来排列宝石。
items = hero.findItems()
# Δ:也许我们应该改变这个功能？
#edges = naiveMaxSum(items)
edges =dynamicMaxSum (items)
x1 = edges[0] * 4 + 4
x2 = edges[1] * 4 + 4
# 从x1收集宝石到x2并转义：
hero.moveXY(x1,x2)

```
