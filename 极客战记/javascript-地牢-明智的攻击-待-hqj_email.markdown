---
layout: default
title: 待
---
## 明智的攻击
```
// Avoid all the fire-traps
// 如果你踩到火焰陷阱，你会烧到。
// 提示1：越大的敌人，血越厚
// 提示2：你不需要杀死所有的食人魔如果你觉得你不够强大的话
// 移动到最近的门
// 用命令 this.attack('门的名字')来打破这个门
// 进入房间
// 攻击房间内的敌人（如何攻击一个没有名字的敌人？）
this.moveUp(2);
this.attack("Door A");
this.moveUp(2);
var enemy1 = this.findNearestEnemy();
this.attack(enemy1);
this.attack(enemy1);
this.attack(enemy1);
this.attack(enemy1);
this.moveDown(3);
this.moveRight(2);
this.moveUp();
this.attack("Door B");
this.moveUp(2);
var enemy2 = this.findNearestEnemy();
this.attack(enemy2);
this.attack(enemy2);
this.moveDown(2);
this.moveRight(2);
this.attack("Door C");
this.moveUp(2);
var enemy3 = this.findNearestEnemy();
this.attack(enemy3);
this.attack(enemy3);
this.attack(enemy3);
this.attack(enemy3);
this.moveDown(2);
this.moveRight(2);
var enemy4 = this.findNearestEnemy();
this.attack(enemy4);
this.attack(enemy4);
var enemy5 = this.findNearestEnemy();
this.attack(enemy5);
this.attack(enemy5);
this.moveUp(3);
this.moveRight();
this.moveDown(4);
this.moveLeft(3);
this.moveDown();
this.moveLeft(2);
// 移动到宝石处
// 攻击敌人
// 得到宝石
// 现在让我们跑吧（移动到 x 标记的位置）
// 再来一次，躲避所有的火焰陷阱
```
