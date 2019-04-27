---
layout: default
title: highlanders
---
## 高地
```

# 你必须击败食人魔
# 但他们正在使用黑魔法！
#只有高地的士兵才能免疫。
# 寻找高地人，他们的名字总是包含“mac”

highlanderName = "mac"

#这个函数应该搜索一个字的字符串：
def wordInString(string, word):
    lenString = len(string)
    lenWord = len(word)
    # Step through indexes (i) from 0 to (lenString - lenWord)
    
        # For each of them through indexes (j) of the word length
    
            # If [i + j]th letter of the string is not equal [j]th letter of world, then break loop
    
            # if [j]th is the last letter of the word (j == lenWord - 1), then return True.
    
    # If loops are ended then the word is not inside the string. Return False.
    
    return True # ∆ Remove this when the function is written.
def wordInText(text, word):
    # 遍历文本中的每个字符。
    for i in range(len(text) - len(word) + 1):
        #为他们每个人循环通过字中的每个字符。
        for j in range(len(word)):
            # Store the shifted index i + j.
            shiftedIndex = i + j
            # 如果移动索引中的字符。
            # 不等于索引“j”中的字中的字符
            if text[shiftedIndex] != word[j]:
                # Break the loop.
                break
            #如果j等于单词中最后一个字母的索引
            if j == len(word) - 1:
                # 那么整个单词就在文本中。
                # 返回True。
                return True
    # 这个词在文本中找不到。返回False。
    return False

# Look at your soldiers and choose highlanders only
soldiers = hero.findFriends()
for soldier in soldiers:
    if wordInText(soldier.id, highlanderName):
        hero.say(soldier.id + " be ready.")
        
# 
hero.say("ATTACK!!!")

```
