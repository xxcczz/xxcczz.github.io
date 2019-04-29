---
layout: default
title: apocalypse
---
## 天启
```

# 炮火的天启在接近我们！
# 在60秒内躲避炮弹。
# 提示：旗子可能派上用场，比如Coinucopia这关。
# 因为每次提交后攻击是随机的，所以你不能简单用 moveXY 把代码写死。

while True:
    flag = hero.findFlag("green")
    if flag:
        hero.pickUpFlag(flag)
    else:
        hero.shield()

```
