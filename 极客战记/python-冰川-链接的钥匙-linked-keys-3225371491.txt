---
layout: default
title: linked-keys
---
## 链接的钥匙
```

# Open doors and collect the chest of gems.

# The nearest peasant has the first key.
peasantLinkedList = hero.findNearest(hero.findFriends())
doorIndex = 0
doorDistance = 12

# The list reference is the reference to the first element.
currentPeasant = peasantLinkedList
while True:
    pos = {"x": 20 + doorIndex * doorDistance, "y": 34}
    hero.command(currentPeasant, "dropItem", pos)
    # Each element of a linked list "links" to the next one
    # Get the next element using currentPeasant.next
    currentPeasant = currentPeasant.next
    # If there is no next element then the list ends.
    if not currentPeasant:
        break
    # Increase "doorIndex" by 1.
    

# Doors are open. Action!

```
