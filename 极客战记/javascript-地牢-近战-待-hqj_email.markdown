---
layout: default
title: 待
---
## 近战
```
this.moveRight();
// 通过上一个关卡，你应该能认识这个。
var enemy1 = this.findNearestEnemy();
// 现在，攻击那个变量，
this.attack(enemy1);
this.attack(enemy1);
this.moveRight(2);
var enemy2 = this.findNearestEnemy();
this.attack(enemy2);
this.moveRight();
```
