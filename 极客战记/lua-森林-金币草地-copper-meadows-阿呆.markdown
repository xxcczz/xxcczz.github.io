---
layout: default
title: copper-meadows
---
## 金币草地
```

-- 收集每片草地的所有金币。
-- 使用旗子在草地间移动。
-- 当你准备好放置旗子时点击“提交”

loop
    local flag = self:findFlag()
    if flag then
        -- 捡起旗子。
        self:pickUpFlag(flag)
    else
        -- 自动移动到你能看见的最近的物品。
        local item = self:findNearestItem()
        if item then
            local position = item.pos
            local x = position.x
            local y = position.y
            self:moveXY(x, y)
        else
            self:say("放置一个旗子给我前往。")
        end
    end
end

```
