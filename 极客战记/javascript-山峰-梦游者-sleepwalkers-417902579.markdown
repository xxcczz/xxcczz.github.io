---
layout: default
title: sleepwalkers
---
## 梦游者
```

var hunter = hero.findNearest(hero.findFriends());
var fenceMap = hunter.getMap();
function convertCoor(row, col) {
return {x: 34 + col * 4, y: 26 + row * 4};
}
var h = 0;
var l = 0;
while(h<fenceMap.length) {
while(l<fenceMap[h].length) {
if (fenceMap[h][l]==1) {
hero.buildXY("fence", convertCoor(h, l).x, convertCoor(h, l).y);
}
l=l+1;
}
h=h+1;
}

```
