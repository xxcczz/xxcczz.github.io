---
layout: default
title: the-gauntlet
---
## 18. 真正的挑战
```
//注意使用钻石升级装备，提高攻击力
// 使用你刚学到的技能击败那些食人魔。
loop {
this.moveRight();
var enemy = this.findNearestEnemy();
this.attack(enemy);
}
```
