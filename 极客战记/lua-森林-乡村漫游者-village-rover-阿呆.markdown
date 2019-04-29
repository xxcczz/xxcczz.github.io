---
layout: default
title: village-rover
---
## 乡村漫游者
```

-- 这定义了findAndAttackEnemy函数
local function findAndAttackEnemy()
    local enemy = hero:findNearestEnemy()
    if enemy then
        hero:attack(enemy)
    end
end
-- 这段代码不是函数的一部分。
while true do
    -- 现在你可以使用findAndAttackEnemy在村子里巡逻
    hero:moveXY(35, 34)
    findAndAttackEnemy()
    
    -- 现在移动到右侧入口。
    hero:moveXY(59, 31)
    -- 使用findAndAttackEnemy
    findAndAttackEnemy()
end

```
