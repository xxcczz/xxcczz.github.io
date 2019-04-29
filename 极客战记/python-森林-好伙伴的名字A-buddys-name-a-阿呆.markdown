---
layout: default
title: buddys-name-a
---
## 好伙伴的名字A
```

# 农民想知道宠物的名字。

# 使用这个函数作为"hear"事件的处理函数。
def sayName(event):
    # 宠物会在函数调用时按顺序说这些。
    pet.say("我名叫狂兽。")
    pet.say("不过我的朋友们叫我毛球。")
    
# 使用pet.on("eventName", functionName)来添加事件监听函数给宠物
# 在这里使用"hear" sayName及pet.on()

pet.on("hear", sayName)
# 你这次不需要说任何东西！
# 农民会进行交谈。

```
