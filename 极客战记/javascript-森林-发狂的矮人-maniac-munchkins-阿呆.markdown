﻿---
layout: default
title: maniac-munchkins
---
## 发狂的矮人
```

// 又一个宝箱等待英雄打开！
// 攻击宝箱来打开它。
// 有些食人魔矮人可不会呆呆地站着挨打！
// 当食人魔离你太近时，你得学着保护你自己

while(true) {
    var enemy = hero.findNearestEnemy();
    var distance = hero.distanceTo(enemy);
    if (hero.isReady("cleave")){
        // 如果劈斩就绪，优先使用劈斩：
        hero.cleave(enemy);}
    else if (distance < 5){
        // 攻击靠近并离你最近的食人魔矮人
        hero.attack(enemy);}
    else{
        // 否则，尝试打开宝箱：
        hero.attack("Chest");}
}

```
