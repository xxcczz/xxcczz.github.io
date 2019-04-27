---
layout: default
title: dread-door
---
## 12. 恐惧之门
```
// 攻击大门(Door)
// 需要攻击很多次,请使用loop循环
loop{
var enemy=this.findNearestEnemy();
if(enemy){
this.attack(enemy);
}
}
```
