---
layout: default
title: copper-meadows
---
## 金币草地
```

// 收集每片草地的所有金币。
// 使用旗子在草地间移动。
// 当你准备好放置旗子时点击“提交”

while(true) {
    var flag = hero.findFlag();
    if (flag) {
        // 捡起旗子。
        hero.pickUpFlag(flag);
    } else {
        // 自动移动到你能看见的最近的物品。
        var item = hero.findNearestItem();
        if (item) {
            var position = item.pos;
            var x = position.x;
            var y = position.y;
            hero.moveXY(x, y);
        }
    }
}

```
