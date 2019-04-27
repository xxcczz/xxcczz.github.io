---
layout: default
title: go-fetch
---
## 去拿过来
```

# 你被困在了陷阱中！
# 派遣宠物拿取治疗药水！

def goFetch():
    # 你可以在处理函数中使用循环。
    while True:
        potion = hero.findNearestItem()
        if potion:
            # 用 “pet.fetch()” 去让你的宠物捡药水：
            pet.fetch(potion)
            pass

# 当宠物被召唤出来时，会触发 "spawn" 事件。
# 这让你的宠物在关卡开始时运行 goFetch()函数。
pet.on("spawn", goFetch)

```
