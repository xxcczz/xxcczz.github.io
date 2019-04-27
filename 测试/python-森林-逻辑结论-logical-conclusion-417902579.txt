---
layout: default
title: logical-conclusion
---
## 逻辑结论
```

# 移动到 Eszter 身边，从他那得到三个密码值
hero.moveXY(24, 16)
secretA = hero.findNearestFriend().getSecretA()
secretB = hero.findNearestFriend().getSecretB()
secretC = hero.findNearestFriend().getSecretC()

# 如果 A 和 B 都为真，或者 C 为真，对 Tamas 说 "TRUE"。否则，说 "FALSE"。
# 记得用上括号好好整理你的逻辑。
tam = (secretA and secretB) or secretC
hero.moveXY(19, 26)
hero.say(tam)

# 如果 A 或 B 为真，并且 C 为真，对 Zsofi 说 "TRUE" 。否则，说 "FALSE"。
zso = (secretA or secretB) and secretC
hero.moveXY(26, 36)
hero.say(zso)

# Say "TRUE" to Istvan if A OR C is true, AND if B OR C is true. Otherwise, say "FALSE."
ist = (secretA or secretC) and (secretB or secretC)
hero.moveXY(37, 34)
hero.say(ist)

# 如果 A 和 B都为真，或者 B 为真而 C 不为真，对 Csilla 说 "TRUE" 。否则，说 "FALSE"。
csi = (secretA and secretB) or (secretB or not secretC)
hero.moveXY(40, 21)
hero.say(csi)

```
