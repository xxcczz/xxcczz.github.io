---
layout: default
title: 待
---
## 地牢40关解救致命地牢
```
//注意插旗位置和时机把握
// 在你救出受酷刑的农民后，逃出地牢。
// 你可以藏在滴水兽后面。
// 杀了警卫会得到不希望的结果。
// 如果你掠夺了所有的宝藏，会得到附件的奖励。
loop {
var flag = this.findFlag();
if (flag) {
this.pickUpFlag(flag);
}
var enemy = this.findNearestEnemy();
var distance = 20 ;
if (enemy !==null) {
distance = this.distanceTo(enemy);
}
if (enemy) {
if (distance < 5) {
this.attack(enemy);
}  
}
var item = this.findNearestItem();
if (item) {
var itemp = item.pos ;
var x = itemp.x ;
var y = itemp.y ;
this.moveXY(x, y);
}
}
```
