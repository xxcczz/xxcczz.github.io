---
layout: default
title: coinucopia
---
## 收集金币
```

// 当你放好旗帜后点 提交。
// 点击提交后，旗帜按钮出现在左下角. 
while(true) {
    var flag = hero.findFlag();
    if (flag) {
        hero.pickUpFlag(flag);
    }
    else {
        hero.say("为英雄放置一面旗帜来移动.");
    }
}

```
