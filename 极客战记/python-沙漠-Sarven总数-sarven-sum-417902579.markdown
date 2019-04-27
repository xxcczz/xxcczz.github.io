---
layout: default
title: sarven-sum
---
## Sarven总数
```

# To disable the fire-traps add the lowest trap.value to the highest value.
# Move to the white X and say the answer to Kitty the cougar.
# Defeat all the ogres if you dare.
# Once all ogres are defeated move to the red X.
# Look out for potions to boost your health.
a=1
whiteX = {'x':27, 'y':42}
redX = {'x':151 , 'y': 118}
while True:
    hero.move(whiteX)
    if hero.pos.x==27:
        break
items = hero.findHazards()
zdz=0
zxz=99999
for item in items:
    if item.value>zdz:
        zdz=item.value
    if item.value<zxz:
        zxz=item.value
sum=zdz+zxz
hero.say(sum)
while True:
    hero.move(redX)
    if hero.pos.x==27:
        break

```
