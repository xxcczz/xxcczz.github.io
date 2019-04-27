---
layout: default
title: if-stravaganza
---
## If的盛宴
```

-- 在食人魔的营地中打败它们！
--循环
while true do
    --找敌人
    local enemy = hero:findNearestEnemy()
    --如果有敌人
    if enemy then        
        -- 攻击敌人
        hero:attack(enemy)
    end
end

```
