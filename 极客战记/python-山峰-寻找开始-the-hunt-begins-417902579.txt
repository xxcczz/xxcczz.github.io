---
layout: default
title: the-hunt-begins
---
## 寻找开始
```

# Senick is trying to find the elusive Burleous Majoris!
# But he doesn't know how big a Burleous Majoris would be...
# Find the average size of this burl population to use as a baseline!

# This function returns average size of all the burls in an array.
def averageSize(burls):
    sum = sumSize(burls)
    # Remember the average is the sum of the parts divided by the amount!
    return sum / burls.length

# This function should return the sum of all the burls sizes.
def sumSize(burls):
    sum=0
    # Implement the sum function using the burls 'size':
    for burl in burls:
        sum=sum+burl.size
    return sum

while True:
    # Find the average size of the burls by calling the 'averageSize' function.
    burls=hero.findEnemies()
    a=averageSize(burls)
    # Say the average size of the seen burls!
    hero.say(a)

```
