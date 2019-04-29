---
layout: default
title: 待
---
## Kithgard精通
```
// 使用移动命令到达迷宫的终点。
// 计算你收集到的宝石数量，然后在到达火球陷阱时通过说出当前的宝石数量来使陷阱失效。
// 在起点的地方会有一只乌鸦告诉你一个密码。在门的附近说出该密码来开门。
// 当你靠近食人魔时杀死它。
// 你可以在需要的时候使用loop来重复所有的指令。
// 如果你通过了这个关卡，你就可以直接跳到边远地区的森林！
this.moveUp();
this.moveRight(3);
this.moveUp();
this.moveDown();
this.moveRight();
this.say("Swordfish");
this.moveRight(2);
this.moveUp();
this.say("1");
this.moveUp(2);
var enemy1 = this.findNearestEnemy();
this.attack(enemy1);
this.attack(enemy1);
this.moveLeft(4);
this.moveUp(3);
this.moveRight(3);
this.moveUp();
this.moveDown();
this.moveRight();
this.say("Swordfish");
this.moveRight(2);
this.moveUp();
this.say("2");
this.moveUp(2);
var enemy2 = this.findNearestEnemy();
this.attack(enemy2);
this.attack(enemy2);
this.moveLeft(4);

```
