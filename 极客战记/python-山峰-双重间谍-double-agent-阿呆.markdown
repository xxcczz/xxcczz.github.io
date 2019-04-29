---
layout: default
title: double-agent
---
## 双重间谍
```

# Find the hidden number in the agent's message to escape.
# Count the number of trailing and leading whitespaces.

# This function returns the coordinates of the n-th passage.
def passagePosByNum(n):
    return {"x": 60, "y": n * 12 + 8}

def onHear(event):
    # The original message.
    message = event.message
    # Trim the message:
    messag = message.trim()
    # The hidden number is the difference of lengths:
    a=len(message)-len(messag)
    # Use passagePosByNum to find the passage to enter:
    b=passagePosByNum(a)
    # Move the pet to the entrance of the passage:
    pet.moveXY(b.x,b.y)
    # Move the pet to the left edge of the map:
    while True:
        x=pet.pos.x-10
        y=pet.pos.y
        pet.moveXY(x,y)

pet.on("hear", onHear)

# The hero should follow the pet.
while True:
    hero.move(pet.pos)

```
