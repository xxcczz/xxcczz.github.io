---
layout: default
title: back-to-back
---
## 背靠背
```

--循环
while true do
    --找敌人
    local enemy = hero:findNearestEnemy()
    --如果有敌人
    if enemy then        
        --攻击
        hero:attack(enemy)
    --否则
    else
        --到中间
        hero:moveXY(40, 36)
    end
end

```
