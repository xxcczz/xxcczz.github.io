---
layout: default
title: logical-path
---
## 逻辑之路
```

-- 从巫师那得到两个秘密的真假值
hero:moveXY(14, 24)
local secretA = hero:findNearestFriend():getSecretA()
local secretB = hero:findNearestFriend():getSecretB()

-- 如果 secretA 和 secretB 都为真，走上面的路；否则，走下面。
-- 查看提示，学会写逻辑表达式。
local secretC = secretA and secretB
if secretC then
    hero:moveXY(20, 33)
else
    hero:moveXY(20, 15)
end
hero:moveXY(26, 24)

-- 如果 secretA 和 secretB 中有一个为真，走上面。
local secretC = secretA or secretB
if secretC then
    hero:moveXY(32, 34)
else
    hero:moveXY(32, 15)
end
hero:moveXY(38, 25)

-- 如果 secretB 不是真的，走上面。
local secretC = secretB
if not secretC then
    hero:moveXY(44, 33)
else
    hero:moveXY(44, 15)
end
hero:moveXY(51, 24)

```
