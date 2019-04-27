---
layout: default
title: anonymous-bank
---
## 匿名银行
```

#找到密码并获取宝藏。

# 我们用编码信息拦截了侦察兵。
message = hero.findNearest(hero.findFriends()).message
# 这里我们将存储密码。
passwords = []
# 所有密码都有5个字母。所有真实密码都有5个字母。
passwordLength = 5
# 使用“;”分割消息 并将这些单词保存在一个变量中。
#使用“;”分割消息并将这些单词保存在一个变量中。
words = message.split(";")
#遍历所有的单词。
for word in words:
    #修剪每个单词以删除空格。
    word = word.trim()
    #如果清理过的单词的长度是5：
    if len(word)==5:
        #将清除的单词添加到密码数组中：
        passwords.append(word)

```
