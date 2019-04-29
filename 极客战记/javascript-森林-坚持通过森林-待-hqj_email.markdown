---
layout: default
title: 待
---
## 坚持通过森林
```
// 使用旗子加入战斗或者撤退。
// If you fail, press Submit again for new random enemies and try again!
// You'll want at least 300 health, if not more.
loop {
var enemy = this.findNearestEnemy();
var flag = this.findFlag();
if(flag) {
// 捡起旗子。
this.pickUpFlag(flag);
} else if (enemy) {
// 打！
if (this.isReady("cleave")) {
this.cleave(enemy);
}
else {
this.attack(enemy);
}
}
}
```
