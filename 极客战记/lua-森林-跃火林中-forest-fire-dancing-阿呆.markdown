﻿---
layout: default
title: forest-fire-dancing
---
## 跃火林中
```

-- 在这关，别碰恶魔石！往其他方向移动避开它们！
while true do
    local evilstone = hero:findNearestItem()
    if evilstone then
        local pos = evilstone:pos
        if pos:x == 34 then
            -- 如果恶魔石在左边，走到右边。
            hero:moveXY(46, 22)
        else
            -- 如果恶魔石在右边，走到左边。
            hero:moveXY(34, 22)
        end
    else
        -- 如果没有恶魔石，那就去到中间。
        hero:moveXY(40, 22)
    end
end

```
