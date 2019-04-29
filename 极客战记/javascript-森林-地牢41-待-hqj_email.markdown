---
layout: default
title: 待
---
## 地牢41
```
// 生存时间比敌人的英雄长！
// 制定自己的战略。有创意!
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
if (this.isReady("cleave")) {
this.cleave(enemy);
}
else {
this.attack(enemy);              
}
}  
}
} 

```
