---
layout: default
title: peasant-protection
---
## 贴身护卫
```

//保护农民
//如果有敌人而且距离太近就攻击
//如果没有敌人就呆在农民旁边
//循环
while(true) {
    //找敌人
    var enemy = hero.findNearestEnemy();
    //如果有敌人
    if (enemy){
        //测距
        var distance = hero.distanceTo(enemy);
        //如果距离小于10
        if (distance < 10){
            //攻击
            hero.attack(enemy);}
        // 否则的话，呆在农民旁边！使用else
        else{
            hero.moveXY(40, 37);
        }
    }

}

```
