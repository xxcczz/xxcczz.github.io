---
layout: default
title: friend-and-foe
---
## 友人和敌人
```

-- 农民和士兵聚集在森林。
-- 命令农民战斗，苦工远离！

while true do
    local friend = hero:findNearestFriend()
    if friend then
        hero:say("To battle, " + friend.id + "!")
    end
    -- 寻找最近的敌人，然后让他们滚蛋
    local enemy = hero:findNearestEnemy()
    if enemy then
        hero:say("To battle, " + enemy.id + "!")
    end
end

```
