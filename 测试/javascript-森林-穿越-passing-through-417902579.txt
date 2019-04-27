---
layout: default
title: passing-through
---
## 穿越
```

// 不要侮辱这个和平食人魔部落

while(true) {
    var item = hero.findNearestItem();
    if(item) {
        // 如果item.type不等于 "gem"
        if(item.type != "gem") {
            // 然后跟随你的宠物。
            hero.moveXY(pet.pos.x, pet.pos.y);
        }
        // 否则:
        else {
            // 移动到宝石的坐标。
            hero.moveXY(item.pos.x, item.pos.y);
        }
    }
}

```
