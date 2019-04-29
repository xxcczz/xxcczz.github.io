---
layout: default
title: 待
---
## 丰富的觅食
```
// 使用 if 和 else if 来处理任何情况
// 放置它来防御敌人，收集金币
// 确保你从物品商店买到伟大的盔甲，建议400点以上的健康。
loop {
var flag = this.findFlag();
var enemy = this.findNearestEnemy();
var item = this.findNearestItem();
if (flag) {
// 当我发现旗子的时候发生了什么？
this.pickUpFlag(flag);
}
else if (enemy) {
// 当我找到敌人的时候发生了什么？
if (this.isReady("cleave")) {
this.cleave(enemy);
}
else {
this.attack(enemy);
}
}
else if (item) {
// 当我找到一个物品的时候，发生了什么？
var itempos = item.pos ;
var x = itempos.x ;
var y = itempos.y ;
this.moveXY(x, y);
}
}
```
