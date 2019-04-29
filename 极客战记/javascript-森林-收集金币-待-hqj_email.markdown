---
layout: default
title: 待
---
## 收集金币
```
// 当你放好旗帜后点提交.
// 点击提交后，旗帜按钮出现在左下角. 
loop {
var flag = this.findFlag();
if (flag) {
this.pickUpFlag(flag);
}
else {
this.say("为英雄放置一面旗帜来移动.");
}
}
```
