---
layout: default
title: sleepwalkers
---
## 梦游者
```

#人类必须生存
#农民必须进村
#这个村庄是一个异常。
#有太多的梦游者，他们经常走出村庄。
#但这只是问题的一半。
#有梦游的英国人，他们跟踪我们的返回农民。
#我们必须建立一个篱笆系统，让睡觉的农民转过身，不要使#用可以唤醒奶酪的战斗方法。
#当有人叫醒他时，Yetis很生气
#Senick是一位经验丰富的猎手，他知道关于yetis的一切。
#他可以计算和预测他们的路线。
#Senick准备了栅栏系统的栅格图。
#你应该使用该方案并在需要的地方建立围栏
#该映射表示为2d数组（数组数组）（1或0）
#0是一个空单元格，
#1是一个建造栅栏的地方

# 我们的梦游农民回来了。
# 但是睡觉的 yetis 也到了。
# 不要把它们唤醒！
#建立围栏让农民通过并停止yetis


#Senick准备了网格地图如何构建栅栏。
hunter = hero.findNearest(hero.findFriends())
fenceMap = hunter.getMap()

# 此功能将网格转换为XY坐标。
def convertCoor(row, col):
    return {'x': 34 + col * 4, 'y': 26 + row * 4}


# 遍历fenceMap并在所有1处构建围栏。
for i in range(len(fenceMap)):
    row = fenceMap[i]
    #现在，行只是另一个数组！
    # 遍历此数组中的所有切片：
    for j in range(len(row)):
        #检查i，j的tile是否为1：
        #hero.buildXY("fire-trap", 36 + 6 * j, 20 + 6 * i)
        tile = fenceMap[i][j]
        if tile ==1:
            hero.buildXY("fence", convertCoor(i, j).x, convertCoor(i, j).y)


# 建筑围栏后移回村庄
hero.moveXY(23, 21)

```
