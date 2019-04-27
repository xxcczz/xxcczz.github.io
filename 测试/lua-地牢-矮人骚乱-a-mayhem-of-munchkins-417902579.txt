---
layout: default
title: a-mayhem-of-munchkins
---
## 矮人骚乱
```

--循环        
while true do
    --找敌人    
    local enemy = hero:findNearestEnemy()        
    --如果敌人存在    
    if enemy then        
        --攻击
        hero:attack(enemy)
    end
end

```
