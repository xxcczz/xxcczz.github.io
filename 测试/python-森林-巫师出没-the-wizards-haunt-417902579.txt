---
layout: default
title: the-wizards-haunt
---
## 巫师出没
```

# 移动到 Zsofia 的身边，从他那得到秘密号码
hero.moveXY(18, 20)
zso = hero.findNearestFriend().getSecret()

# 将 Zsofia 的数字除以 4 得到 Mihaly 的数字。
# Move to Mihaly and say his magic number.
mih = zso / 4
hero.moveXY(30, 15)
hero.say(mih)

# 把 Mihaly 的号码除以来得到 Beata 的号码
# Move to Beata and say her magic number.
bea=mih/5
hero.moveXY(42, 21)

hero.say(bea)
# 将 Beata 的数字减去 Mihaly 的数字得到 Sandor 的数字。
# Move to Sandor and say his magic number.
san=mih-bea
hero.moveXY(38, 36)
hero.say(san)

```
