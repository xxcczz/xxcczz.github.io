---
layout: default
title: 待
---
## 金币草地
```
// 收集每片草地的所有金币。
// 使用旗子在草地间移动。
// 当你准备好放置旗子时点击“提交”
loop {
var flag = this.findFlag();
if (flag) {
// 捡起旗子。
this.pickUpFlag(flag);
} else {
// 自动移动到你能看见的最近的物品。
var item = this.findNearestItem();
if (item) {
var position = item.pos;
var x = position.x;
var y = position.y;
this.moveXY(x, y);
}
}
}
```
