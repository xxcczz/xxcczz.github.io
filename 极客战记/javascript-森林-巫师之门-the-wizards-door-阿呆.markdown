---
layout: default
title: the-wizards-door
---
## 巫师之门
```

// Move to Laszlo and get his secret number.
hero.moveXY(30, 13);
var las = hero.findNearestFriend().getSecret();

// 向 Laszlo 的数字中加7就能得到 Erzsebet的号码
// Move to Erzsebet and say her magic number.
var erz = las + 7;
hero.moveXY(17, 26);
hero.say(erz);

// 将 Erzsebet 的数字除以 4 得到 Simoyi 的数字。
// Go to Simonyi and tell him his number.
var sim=erz/4;
hero.moveXY(30, 39);
hero.say(sim);
// 将 Simonyi 的数字乘以 Laszlo 的数字得到 Agata 的数字。
// Go to Agata and tell her her number.
var aga=sim*las;
hero.moveXY(43, 27);
hero.say(aga);

```
