---
layout: default
title: backwoods-fork
---
## 边地之叉
```

// 一大波食人魔正在到来！
// 使用 checkAndAttack 函数让代码易读。

// 这个函数有一个参数。
// 参数是一种给函数传递信息的方式。
function checkAndAttack(target) {
    // target参数只是一个变量！
    // 它包含了函数调用时的参数。
    if (target) {
        hero.attack(target);}
    hero.moveXY(43, 34);
}
while(true) {
    hero.moveXY(58, 52);
    var topEnemy = hero.findNearestEnemy();
    checkAndAttack(topEnemy);
    
    // 移动到底部的X标记处。
    hero.moveXY(58, 16);
    // 创建名为 bottomEnemy 的变量，寻找最近敌人。
    var bottomEnemy = hero.findNearestEnemy();
    // 使用 checkAndAttack 函数，并使用 bottomEnemy 变量。
    checkAndAttack(bottomEnemy);
}

```
