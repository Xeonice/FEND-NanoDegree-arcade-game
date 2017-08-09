# FEND NanoDegree-arcade-game
[TOC]
## 简介
该项目依照NanoDegree P5要求制作，在标准模版的基础之上进行了部分修改。
## 结构说明
该程序包括一个Enemy对象，一个Player对象，以及
### Object Enemy
`this.x`与`this.y`确定敌人当前位置。
`this.sprite`导入敌人的预设图片。
`this.speed`利用随机数确定敌人的初始速度。
### Enemy.prototype.update
`this.x += this.speed * dt;`保证敌人在每一台电脑上都以固定速度运行。
`if`语句通过重置坐标使敌人能够从左至右不断出现。
### Enemy.prototype.render
画出敌人。
### Object Player
`this.x`与`this.y`确定玩家当前位置。
`this.sprite`导入玩家的预设图片。
### Player.prototype.update
通过`if`，先判断玩家y坐标是否抵达地图最上处，满足条件使提示玩家胜利，并重置坐标。
**PS：count为延时技巧，意在延迟提示信息的出现。**
### Player.prototype.render
画出玩家。
### Player.prototype.handleInput
运用`switch`语句判断当前按键指令，并依据输入指令对x，y坐标进行加减操作。
### Player.prototype.checkCollisions
碰撞判断函数，先判断player与enemy的y坐标是否相同，从而确定player与enemy是否处于同一行，其次，判断enemy的x坐标与player的x坐标之差的绝对值是否小于40，满足，则重置玩家位置至原点。
## 操作说明
游戏使用方向键⬆️⬇️⬅️➡️控制，目标为在不碰触Bugs的前提下成功抵达河对岸。


