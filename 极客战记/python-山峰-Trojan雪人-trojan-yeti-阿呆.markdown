---
layout: default
title: trojan-yeti
---
## Trojan雪人
```

# You need to defeat ogres.
# Send wereyeti peasants to the ogre camp and watch.

# This function returns a friendly unit by the name.
def findFriendByName(name):
    friends = hero.findFriends()
    for i in range(len(friends)):
        if friends[i].id == name:
            return friends[i]
    return None

# The sergeant wrote the list of wereyeti peasants' names.
sergeant = hero.findNearest(hero.findFriends())
wereList = sergeant.wereList
# The list isn't clean and contains redundant spaces. 
wereNames = wereList.split(",")
#hero.say(wereNames)
# Iterate through wereNames array:
for name in wereNames:
    # Trim the whitespace from the name
    # and save it in the new variable:
    #hero.say(name)
    name1 = name.trim()
    #hero.say(name1)
    # Use findFriendByName function to find a wereyeti:
    #hero.say(findFriendByName(name1))
    a=findFriendByName(name1)
    if a:
        # Command that unit move to the ogre camp:
        hero.command(a, "move", {"x": 48, "y": 48})

```
