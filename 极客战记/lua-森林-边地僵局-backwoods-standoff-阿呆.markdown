---
layout: default
title: backwoods-standoff
---
## 边地僵局
```

--循环
while true do
    --找敌人
    local enemy = hero:findNearestEnemy()
    --如果有敌人
    if enemy then
        --如果技能劈斩准备好了
        if hero:isReady("cleave") then
            --劈斩
            hero:cleave(enemy)
        -- 否则
        else
            --普通攻击
            hero:attack(enemy)
        end
    end
end

```
