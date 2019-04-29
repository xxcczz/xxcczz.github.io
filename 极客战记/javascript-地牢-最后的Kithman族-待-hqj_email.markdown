---
layout: default
title: 待
---
## 最后的Kithman族
```
// 使用loop循环移动并攻击目标
loop {
this.moveRight();
this.moveUp();
var enemy = this.findNearestEnemy();
this.attack(enemy);
this.moveRight();
this.moveDown(2);
this.moveUp();
}
```
