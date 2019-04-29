---
layout: default
title: summits-gate
---
## 峰会之门
```

local function bz1()
    for i=1, #friends do
        local friend = friends[i]
        if friend.type == "paladin" then
            bz3(friend)
        else
            bz4(friend)
        end
    end
end
local function bz2()
    local catapult = hero:findNearest(hero:findByType("catapult"))
    local enemy = hero:findNearestEnemy()
    if catapult then
        hero:attack(catapult)
    elseif enemy then
        hero:attack(enemy)
    end
end
local function bz3(paladin)
    local lowestFriend = bz5()
    if self.health < 3500 then
        hero:command(paladin, "cast", "heal", self)
    elseif lowestFriend then
        hero:command(paladin, "cast", "heal", lowestFriend)
    else
        hero:command(paladin, "move", hero.pos)
    end
end
local function bz4(friend)
    local enemy = friend:findNearestEnemy()
    if enemy then
        hero:command(friend, "attack", enemy)
    elseif not enemy then
        hero:command(friend, "move", hero.pos)
    end
end
local function bz5()
    local lowestHealth = 99999
    local lowestFriend = nil
    for i=1, #friends do
        local friend = friends[i]
        if friend.type == "paladin" then
            if friend.health < lowestHealth and friend.health < friend.maxHealth then
                lowestHealth = friend.health
                lowestFriend = friend
            end
        end
    end
    return lowestFriend
end
local function bz6()
    local tower = hero:findNearest(hero:findByType("tower"))
    local enemy = hero:findNearestEnemy()
    if tower then
        hero:attack(tower)
    elseif enemy then
        hero:attack(enemy)
    end
end
local function bz7()
    local warlock = hero:findNearest(hero:findByType("warlock", hero:findEnemies()))
    if warlock then
        hero:say("attack" .. warlock)
        hero:attack(warlock)
    end
end
local function bz8()
    for i=1, #friends do
        local friend = friends[i]
        local enemy = hero:findNearestEnemy()
        if friend.type == "paladin" then
            bz3(friend)
        else
            if enemy then
                hero:command(friend, "attack", enemy)
            else
                hero:command(friend, "move", {x=320,y=30})
            end
        end
    end
end
local function bz9()
    if self.gold >= self:costOf("archer") then
        self:summon("archer")
    end
end
local function pickUpCoin()
    local item = hero:findNearest(hero:findByType("gem"))
    if item then
        hero:moveXY(item.pos.x, item.pos.y)
    end
end
local function bz10()
    local witch = hero:findNearest(hero:findByType("witch", hero:findEnemies()))
    local skeleton = hero:findNearest(hero:findByType("skeleton", hero:findEnemies()))
    local enemy = hero:findNearestEnemy()
    if skeleton then
        hero:attack(skeleton)
    elseif witch then
        hero:attack(witch)
    else
        hero:attack(enemy)
    end
end
local function bz11()
    while hero.health<3500 do
        bz1()
    end  
end
while true do
    if hero.pos.x < 92 then
        local friends = self:findFriends()
        bz1()
        bz2()
    elseif hero.pos.x >=92 and hero.pos.x < 170 then
        local friends = self:findFriends()
        bz1()
        bz6()
        local enemy = hero:findNearestEnemy()
        if not enemy then
            
            hero:moveXY(171, 14)
            bz1()--奶爸快点过来
            hero:wait(4)
            bz11()
            hero:moveXY(230, 14)
            bz1()--奶爸快点过来
            hero:wait(4)
        end
    elseif hero.pos.x >= 170 and hero.pos.x < 245 then
        local distance = hero:distanceTo(hero:findNearest(hero:findByType("paladin")))
        if distance < 25 then
            hero:moveXY(270, 34)
            bz1()
        end
    elseif hero.pos.x >= 245 and hero.pos.x < 280 then
        bz7()
        local friends = self:findFriends()
        bz8()
        local warlock = hero:findNearest(hero:findByType("warlock", hero:findEnemies()))
        if not warlock then
            hero:moveXY(280, 34)
        end
    elseif hero.pos.x >= 280 and hero.pos.x < 350 then
        bz9()
        local friends = self:findFriends()
        bz8()
        bz10()
    end
end

```
