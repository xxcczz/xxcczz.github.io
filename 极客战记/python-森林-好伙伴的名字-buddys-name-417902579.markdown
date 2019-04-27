---
layout: default
title: buddys-name
---
## 好伙伴的名字
```

# 我们需要知道新宠物的名字。

# 把这个函数用作宠物 "hear" 事件的处理函数。
def onHear(event):
    # 不要更改这个函数
    pet.say("喵呜~ 汪 喵呜~")
    pet.say("汪 汪")
    pet.say("喵呜~")
    pet.say("喵呜~")
    pet.say("喵呜~ 汪 喵呜~ 喵呜~")

# 使用 “the pet.on(eventType，eventHandler) 方法”
# 指派onHear函数来处理"hear"事件。
pet.on("hear", onHear)

# 这必须在 "pet.on" 的后面。
hero.say("伙计，你叫什么名字？")
hero.say("能重复一次吗？")

```
