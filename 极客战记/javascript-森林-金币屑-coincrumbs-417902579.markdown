---
layout: default
title: coincrumbs
---
## 金币屑
```

// 跟随硬币的轨迹来到红色 X 标记的出口

while(true) {
    // 这能找到最近的敌人。
    var item = hero.findNearestItem();
    if (item){
        // 这将物品的 pos，就是坐标，存储在变量中。
        var itemPosition = item.pos;
        // 将物品的 X 和 Y 坐标放进变量。
        var itemX = itemPosition.x;
        var itemY = itemPosition.y;
        // Now, use moveXY to move to itemX and itemY:
        hero.moveXY(itemX, itemY);}
}

```
