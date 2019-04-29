---
layout: default
title: 待
---
## 多人游戏之林
```
// 当第一个收集100个金币的人！
// 如果你死了，重生的时候只有原来金币的67%
loop {
// 找到金币并攻击敌人
// 使用旗子和特殊的移动策略来赢得比赛！
var flag = this.findFlag ();
var item = this.findNearestItem();
var enemy =this.findNearestEnemy();
if (enemy !== null) {
var distance = this.distanceTo(enemy);
}
if (flag) {
this.pickUpFlag(flag);
}
else if (distance < 5 ) {
this.attack(enemy);
}
else {
var itempos = item.pos ;
var x = itempos.x ;
var y = itempos.y ;
this.moveXY(x, y);
}
}
```
