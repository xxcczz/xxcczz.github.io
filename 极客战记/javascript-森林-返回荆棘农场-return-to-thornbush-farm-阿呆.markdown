---
layout: default
title: return-to-thornbush-farm
---
## 返回荆棘农场
```

// 这个函数 “maybeBuildTrap” 定义了两个参数
function maybeBuildTrap(x, y) {
    // 使用x和y作为移动的坐标。
    hero.moveXY(x, y);
    var enemy = hero.findNearestEnemy();
    if (enemy) {
        // 使用 buildXY 在特定 x 和 y 处建造 "fire-trap".
        hero.buildXY("fire-trap", x, y);
    }
}
while (true) {
    // 这会调用 maybeBuildTrap，并使用上方入口的坐标。
    maybeBuildTrap(43, 50);
    // 下面在左侧入口使用maybeBuildTrap！
    maybeBuildTrap(25, 33);
    // 在底部入口处使用“maybeBuildTrap” ！
    maybeBuildTrap(42, 21);
}

```
