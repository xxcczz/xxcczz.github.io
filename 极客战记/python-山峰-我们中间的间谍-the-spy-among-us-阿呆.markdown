---
layout: default
title: the-spy-among-us
---
## 我们中间的间谍
```

#城墙很坚固。
#但是，其中一个农民是间谍！
#提示:间谍的名字有字母“z”

#此函数检查单词中的特定字母。
#一个字符串只是一个数组！ 像数组一样循环它
def letterInWord(word, letter):
    for i in range(len(word)):
        character = word[i]
        #如果字符等于字母，则返回True
        if character==letter:
            return True
    #字母不在这个单词中，所以返回False
    return False


spyLetter = "z"
friends = hero.findFriends()

for friend in friends:
    friendName = friend.id
    if letterInWord(friendName, spyLetter):
        #揭示间谍！
        hero.say(friendName + " is a spy!")
    else:
        hero.say(friendName + " is a friend.")

```
