---
layout: default
title: woodland-cleaver
---
## 森林劈斩者
```

// 尽可能经常使用你的新技能“cleave”
//移动
hero.moveXY(23, 23);
//循环
while(true) {
    //找敌人
    var enemy = hero.findNearestEnemy();
    //如果技能劈斩准备好了
    if (hero.isReady("cleave")){
        //劈斩
        hero.cleave(enemy);}
    //否则
    else{
        //普通攻击
        hero.attack(enemy);}
}

```
