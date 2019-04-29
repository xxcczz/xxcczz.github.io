---
layout: default
title: 待
---
## Agrippa防守
```
loop {
var enemy = this.findNearestEnemy();
if(enemy) {
// 用 distanceTo 获取与敌人的距离。
var distance = this.distanceTo(enemy);
// 如果距离小于5米...
if (distance < 5) {
if (this.isReady("cleave")) {
// ...如果 “cleave”技能准备好了，就“cleave”掉他们！
this.cleave(enemy);
}
else {
this.attack(enemy);
// ...否则，仅仅进行普通攻击。
}
} 
}
}
```
