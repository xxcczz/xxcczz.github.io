---
layout: default
title: blind-distance
---
## 盲距
```

// 你的任务是告诉他兽人的距离。

// 这个函数寻找最近的敌人，并返回距离。
// If there is no enemy, the function returns 0.

function nearestEnemyDistance() {
    var enemy = hero.findNearestEnemy();
    var result = 0;
    if (enemy){
         result = hero.distanceTo(enemy);}
    return result;
}
while(true) {
    // Call nearestEnemyDistance() and
    // save the result in the variable enemyDistance.
    var enemyDistance = nearestEnemyDistance();
    // If the enemyDistance is greater than 0: 
    if (enemyDistance>0){
        // Say the value of enemyDistance variable.
        hero.say(enemyDistance);}
}

```
