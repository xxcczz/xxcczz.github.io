---
layout: default
title: gridmancer-redux
---
## Gridmancer归途
```

array_greed = hero.navGrid
def getRectngle(index1, index2):
    width = 0
    height = 0
    if array_greed[index1][index2] == 'Coin':
        indy = index2
        indx = index1
        for x in range(indx, lenght_xy):
            if array_greed[x][indy] == 'Coin':
                width = width + 1
            else:
                break
        for y in range(indy, lenght_xy):
            width_tmp = 0
            for x in range(indx, lenght_xy):
                width_tmp = width_tmp + 1
                if array_greed[x][y] != 'Coin':
                    return_object = {'x': index1, 'y': index2, 'width': width, 'height': height}
                    return return_object
                elif (width_tmp >= width):
                    height = height + 1
                    break
        return_object = {'x': index1, 'y': index2, 'width': width, 'height': height}
        return return_object
    else:
        return None
rect = []  # {x, y, w, h}
lenght_xy = 20
for x in range(lenght_xy):
    for y in range(lenght_xy):
        rectg = getRectngle(x, y)
        if rectg:
            rect.push(rectg)
            for xi in range(rectg.x, rectg.x + rectg.width):
                for yi in range(rectg.y, rectg.y + rectg.height):
                    array_greed[xi][yi] = 'Got'
index = 0
break_i = 56
for rec in rect:
    hero.addRect(rec.x, rec.y, rec.width, rec.height)
    if break_i == index:
        hero.say([rect[index].x, rect[index].y, rect[index].width, rect[index].height])
        break
    index = index + 1

```
