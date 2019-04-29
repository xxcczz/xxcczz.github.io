---
layout: default
title: adventure-time
---
## 10. 冒险时刻
```

spawnTime = 0
while True:
    if game.time > spawnTime:
        game.spawnXY("munchkin", 20, 40)
        # Next spawnTime set to current game.time + 2
        spawnTime = game.time + 2

var spawnTime = 0;
while(true) {
    if(game.time > spawnTime) {
        game.spawnXY("munchkin", 20, 40);
        // Next spawnTime set to current game.time + 2 
        spawnTime = game.time + 2;
    }
}

# game.time是游戏过去的时间
game.spawnPlayerXY("guardian", 10, 35)
game.addSurviveGoal()
game.addDefeatGoal(5)

def onSpawn(event):
    while True:
        unit = event.target
        enemy = unit.findNearestEnemy()
        if enemy:
            unit.attack(enemy)

game.setActionFor("munchkin", "spawn", onSpawn)

# game.time从零开始，并在几秒内向上计数
spawnTime = 0
while True:
    # 产生时间是我们想要产生的时间。
    if game.time > spawnTime:
        pass
        # 在60, 35产生一个“munchkin”
        game.spawnXY("munchkin", 60, 35)
        # 设置spawnTime等于game.time + 2
        # 所以敌人会每2秒产生一次。
        spawnTime = game.time + 2

```
