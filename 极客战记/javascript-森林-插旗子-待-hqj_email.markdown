---
layout: default
title: 待
---
## 插旗子
```
// 在你想要建造陷阱的位置插旗
// 当你没有在建造陷阱的时候，收集金币！
loop {
var flag = this.findFlag();
if (flag) {
// 我们该如何通过旗子的位置得到 fx 和 fy 呢？
// （向下看如何得到物品的 x 和 y）
var flagpos = flag.pos ;
var fx = flagpos.x ;
var fy = flagpos.y ;
this.buildXY("fire-trap", fx, fy);
this.pickUpFlag(flag);
}
else {
var item = this.findNearestItem();
if (item) {
var itemPos = item.pos;
var itemX = itemPos.x;
var itemY = itemPos.y;
this.moveXY(itemX, itemY);
}
}
}
```
