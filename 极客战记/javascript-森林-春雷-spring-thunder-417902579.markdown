---
layout: default
title: spring-thunder
---
## 春雷
```

// 某些硬币和宝石吸引闪电。
// 这个英雄应只收集银币和蓝宝石

while (true) {
    var item = hero.findNearestItem();
    // 一枚银币的价值为2。
    // 如果item.type等于“coin”，则收集
    // AND item.value 相等于2
    if (item.type == "coin" && item.value == 2) {
        hero.moveXY(item.pos.x, item.pos.y);
    }
    // 一个蓝宝石价值10
    // 如果item.type等于“gem”，则收集
    // AND item.value等于10。
    if (item.type == "gem" && item.value == 10) {
        hero.moveXY(item.pos.x, item.pos.y);
    }}

```
