---
layout: default
title: mind-the-trap
---
## 小心陷阱
```

-- 如果你试图攻击一个远处的敌人，你的英雄会忽略掉所有的旗子而朝它冲过去。
-- 你需要确保你只攻击靠近自己的敌人！

while true do
    local flag = hero:findFlag()
    local enemy = hero:findNearestEnemy()
    
    if flag then
        -- 去拔旗子。
        hero:pickUpFlag(flag)
        hero:say("我应该去把旗子拔起来。")
    elseif enemy then
        -- 仅当敌人的距离小于10米时才攻击。
        if hero:distanceTo(enemy)<10 then
            if hero:isReady("cleave") then
                hero:cleave(enemy)
            else
                hero:attack(enemy)
            end
        end
    end
end

```
