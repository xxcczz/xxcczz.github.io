---
layout: default
title: precision-kicking
---
## 精准逆转
```

#推球击倒所有蓝色骨骼而不击中任何红色骨骼。
#蓝色骷髅可以被发现为敌人。
friends = hero.findFriends()
friend=friends[0]
balls = hero.findByType("ball")
ball=balls[0]
x1=ball.pos.x
y1=ball.pos.y
jd=0
drs = hero.findEnemies()
while True:
    jd=jd+1
    x=x1+3*Math.cos(jd/180*Math.PI)
    y=y1+3*Math.sin(jd/180*Math.PI)
    hero.command(friend, "move", {"x": x, "y": y})
    if ball.pos.x==x1 and ball.pos.y==y1:
        xl1=Vector.subtract(ball.pos,friend.pos)
        for dr in drs:
            if dr.health<=0:
                continue
            xl2=Vector.subtract(dr.pos,ball.pos)
            xl3=Vector.subtract(dr.pos,friend.pos)
            distance1 = xl1.magnitude()
            distance2 = xl2.magnitude()
            distance3 = xl3.magnitude()
            if distance1+distance2-distance3<0.001:
                hero.command(friend, "move", {"x": x1, "y": y1})
                break

friends = hero.findFriends()
friend=friends[0]
balls = hero.findByType("ball")
ball=balls[0]
x1=ball.pos.x
y1=ball.pos.y
jd=-90
r=10
while True:
    if ball.pos.x!=x1 and ball.pos.y!=y1:
        continue
    #hero.say(jd)
    polarPos=jd/180*Math.PI
    x=x1+r*Math.cos(polarPos)
    y=y1+r*Math.sin(polarPos)
    hero.command(friend, "move", {"x": x, "y": y})
    enemies = hero.findEnemies()
    for j in range(len(enemies)):
        enemy = enemies[j]
        cd1=Vector.subtract(ball.pos,friend.pos).magnitude()
        cd2=Vector.subtract(enemy.pos,ball.pos).magnitude()
        cd3=Vector.subtract(enemy.pos,friend.pos).magnitude()
        if cd1+cd2-cd3<=0.0005:
            hero.command(friend, "move", {"x": x1, "y": y1})
            while 1:
                if ball.pos.x!=x1 and ball.pos.y!=y1:
                    break
            hero.command(friend, "move", {"x": x, "y": y})
            hero.wait(2)
            break
    jd=jd-1
    jd=jd % 360

# Push the ball to knock over all the blue skeletons without hitting any red ones.
# The blue skeletons can be found as enemies.
center = Vector(40, 35)
punch_array = []
enemies = hero.findEnemies()
friend = hero.findFriends()[0]
ball = self.findNearest(self.findByType('ball'))
ballPoss = Vector(ball.pos.x, ball.pos.y)
for enemy in enemies:
    s2b = Vector.multiply(Vector.normalize(Vector.subtract(ballPoss, enemy.pos)), 7)
    b2p = ball.pos.add(s2b)
    punch_array.append(b2p)

distance = 100
while len(punch_array) > 0:
    min_dist, min_index = 999, -1
    for index, punch in enumerate(punch_array):
        if min_dist > Vector.subtract(punch, friend.pos).magnitude():
            min_dist = Vector.subtract(punch, friend.pos).magnitude()
            min_index = index
    vector = punch_array.pop(min_index)
    hero.command(friend, 'move', vector)
    hero.wait(1)
    hero.command(friend, 'move', center)
    hero.wait(1)
    hero.command(friend, 'move', vector)

```
