---
layout: default
title: slumbering-sample
---
## 睡眠样本
```

# One last stop before the plan can be set into motion!
# It's up to you to help Senick get the average size of these yetis.
def pj(yetis):
    sum=0
    for yeti in yetis:
        sum=sum+yeti.size
    return sum/len(yetis)
# Find all the Yetis using 'findByType':
yetis = hero.findByType("yeti")
# Implement the averageSize function from scratch:

# Say the average size of the yetis:
hero.say(pj(yetis))

```
