---
layout: default
title: drop-the-flag
---
## 插旗子
```

-- 在你想要建造陷阱的位置插旗
-- 当你没有在建造陷阱的时候，收集金币！

loop
    local flag = self:findFlag()
    if flag then
        -- 我们该如何通过旗子的位置得到 flagX 和 flagY 呢？
        -- （向下看如何得到物品的 x 和 y）
        local flagX = flag.pos.x
        local flagY = flag.pos.y
        self:buildXY("fire-trap", flagX, flagY)
        self:pickUpFlag(flag)
    else
        local item = self:findNearestItem()
        if item then
            local itemPos = item.pos
            local itemX = itemPos.x
            local itemY = itemPos.y
            self:moveXY(itemX, itemY)
        end
    end
end

```
