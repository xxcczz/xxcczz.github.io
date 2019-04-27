---
layout: default
title: coincrumbs
---
## 金币屑
```

-- 跟随硬币的轨迹来到红色 X 标记的出口

while true do
    -- 这能找到最近的敌人。
    local item = hero:findNearestItem()
    if item then
        -- 这将物品的 pos，就是坐标，存储在变量中。
        local itemPosition = item.pos
        -- 将物品的 X 和 Y 坐标放进变量。
        local itemX = itemPosition.x
        local itemY = itemPosition.y
        -- Now, use moveXY to move to itemX and itemY:
        hero:moveXY(itemX, itemY)
    end
end

```
