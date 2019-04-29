---
layout: default
title: buddys-name-b
---
## 好伙伴的名字 B
```

# 宠物需要向英雄和农民问好。

# 使用这个函数作为"hear"事件的处理函数:
def sayHello(event):
    # 宠物在说你好：
    pet.say("致敬")

# 使用宠物的.on("eventType", functionName)方法.
# 这一关里，宠物需要在听到声音后运行sayHello
pet.on("hear", sayHello)

# 那么，问候宠物，等待回应。
hero.say("你好，朋友！")

```
