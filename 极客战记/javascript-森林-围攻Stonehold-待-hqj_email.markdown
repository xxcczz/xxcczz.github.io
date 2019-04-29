---
layout: default
title: 待
---
## 围攻Stonehold
```
// Help your friends beat the minions that Thoktar sends against you.
// 你需要更好的装备和策略去赢得战斗。
// 标记可能有用，不过它由你决定——要有创造性哦！
loop {
var flag = this.findFlag();
var enemy = this.findNearestEnemy();
var item = this.findNearestItem();
if (flag) {
this.pickUpFlag(flag);
}
else if (enemy) {
if (this.isReady("cleave")) {
this.cleave(enemy);
}
else {
this.attack(enemy);
}      
}
if (item) {
var itempos = item.pos;
var x = itempos.x ;
var y = itempos.y ;
this.moveXY(x, y);
}
}
```
