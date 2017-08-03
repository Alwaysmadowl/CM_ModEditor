# 事件

事件类: 以下函数为hook函数, 当游戏执行到以下事件便会执行对应的函数

---

* ### 添加技能按钮：技能x

  ![](/assets/添加技能按钮.png)

为玩家添加一个技能按钮

作为事件的开端：在游戏中点击按钮，就会执行这块积木下面的积木脚本。

还可以把“技能X”替换为你想要的文本，给按钮起名字。

在游戏界面右上角会看到一个“技能键”的按钮。

![](https://images-cdn.shimo.im/6qth8wzpYX0eIeaP/image.png!thumbnail)

点击展开就可以看到自己定义的技能按钮，每使用一个该积木就会多一个按钮。

![](https://images-cdn.shimo.im/vHk5zOPmzd4yFW6Z/image.png!thumbnail)

* ### 当方块被点击

### ![](/assets/当方块被点击.png)

function useItem \(x, y, z, itemId, blockId, side, itemDamage, blockDamage\)

参数包括

* x, y, z
* itemId : 手持物品ID
* blockId : 被点击方块ID
* side : 被点击的面
* itemDamage : 手持物品信息
* blockDamage : 被点击方块信息 

事件的开端：当方块被点击的时候就会执行这块积木下面的积木脚本。

以下参数积木可以作用于该积木。

* x, y, z

![](https://images-cdn.shimo.im/Wvb8cBbGVIgzjAcX/%E4%BD%8D%E7%BD%AE.png!thumbnail)

* 手持物品

![](https://images-cdn.shimo.im/S345E0RbZdw5t6Bd/%E6%89%8B%E6%8C%81%E7%89%A9%E5%93%81.png!thumbnail)

* 被点击方块

![](https://images-cdn.shimo.im/bOYBln8EKTYoxUds/%E6%96%B9%E5%9D%97id.png!thumbnail)

* 被点击的面

![](https://images-cdn.shimo.im/dcKd4MeU2JcDcocy/%E6%96%B9%E5%90%91.png!thumbnail)

* 手持物品损坏值

![](https://images-cdn.shimo.im/vQlm5LNr0wokffjl/%E6%89%8B%E6%8C%81%E7%89%A9%E5%93%81%E5%B1%9E%E6%80%A7.png!thumbnail)

* 被点击方块损坏值

![](https://images-cdn.shimo.im/3EPOSUHIJVAVetMo/%E6%96%B9%E5%9D%97%E5%B1%9E%E6%80%A7.png!thumbnail)

### 当方块被破坏

![](/assets/当方块被破坏.png)

* function destroyBlock \(x, y, z, side\)

* 参数

  * x, y, z

  * side : 被点击的面

* 事件的开端：当方块被破坏的时候就会触发该事件，马上执行这块积木下面的积木脚本。
* 以下参数积木可以作用于该积木。



* x, y, z

![](https://images-cdn.shimo.im/Wvb8cBbGVIgzjAcX/%E4%BD%8D%E7%BD%AE.png!thumbnail)

* 被点击的面

* ![](https://images-cdn.shimo.im/dcKd4MeU2JcDcocy/%E6%96%B9%E5%90%91.png!thumbnail)

* ### 当开始破坏方块

  ![](/assets/当开始破坏方块.png)

function startDestroyBlock \(x, y, z, side\)

参数

* x, ,y ,z
* side : 被点击的面

事件的开端：当开始破坏方块（方块不一定被破坏）的时候就会触发该事件，马上执行这块积木下面的积木脚本。

以下参数积木可以作用于该积木。

* x, y, z

![](https://images-cdn.shimo.im/Wvb8cBbGVIgzjAcX/%E4%BD%8D%E7%BD%AE.png!thumbnail)

* 被点击的面

* ![](https://images-cdn.shimo.im/dcKd4MeU2JcDcocy/%E6%96%B9%E5%90%91.png!thumbnail)

* ### 当初始化游戏

  * ![](/assets/当初始化游戏.png)
* * function newLevel\(\)
* ### 当离开游戏

  * ![](/assets/当离开游戏.png)
* * function leaveGame\(\)
* ### 当实体被攻击

  * ![](/assets/当实体被攻击.png)

  * function attackHook\(attacker, victim\)

  * 参数

    * attacker :  攻击者

    * victim :  被攻击者
* ### 当投掷物砸中实体

  * ![](/assets/当抛掷物砸中实体.png)

  * function projectileHitEntityHook\(projectile, target\)

  * 参数

    * projectile : 投掷物

    * target : 被砸中实体
* ### 当投掷物砸中方块

  * ![](/assets/当投掷物砸中方块.png)

  * function projectileHitBlockHook\(Projectile, blockX, blockY, blockZ, side

  * 参数

    * Projectile : 投掷物

    * blockX,** **blockY, blockZ : 坐标

    * side : 被砸中的面
* ### 当爆炸发生

  * ![](/assets/当爆炸发生.png)

  * function explodeHook\(ent, x, y, z, power, onFire\)

  * 参数

    * ent : 爆炸物

    * power : 爆炸范围

    * onFire : 是否着火
* ### 当玩家有吃的项

  * ![](/assets/当玩家有吃的项.png)
  * function eatHook\(hearts, saturationRatio\)
* ### 当实体已经遭受损害

  * ![](/assets/当实体已经遭受损害.png)

  * function entityHurtHook\(attacker, victim, hearts\)

  * 参数

    * attacker :  攻击者

    * victim :  被攻击者

    * hearts : 伤害值
* ### 当玩家拿起经验球

  * ![](/assets/当玩家拿起经验值球.png)

  * function playerAddExpHook\(player, experienceAdded\)

  * 参数

    * player : 捡起经验球的实体

    * experienceAdded : 获取的经验值多少; 大经验球:7, 中经验球:3,小经验球:1
* ### 循环调用

  * ![](/assets/循环调用.png)

  * 该函数每0.05秒调用一次

  * function modTick\(\)
* ### 当发送聊天信息

  * ![](/assets/当发送聊天信息.png)

  * function chatHook\(text\)

  * 参数

    * text : 消息内容
* ### 当输入命令

  * ![](/assets/当输入命令.png)

  * function procCmd \(cmd\)

  * 参数

    * cmd : 指令
* ### 当实体死亡

  * ![](/assets/当实体死亡.png)
  * function deathHook\(attacker, victim\)
  * 参数
    * attacker : 攻击者
    * victim : 被攻击者
* ### 当实体消失

  * ![](/assets/当实体消失.png)

  * function entityRemovedHook\(entity\)

  * 参数

    * entity : 实体
* ### 当添加实体

  * ![](/assets/当添加实体.png)

  * function entityAddedHook\(entity\)

  * 参数

    * entity: 实体
* ### 当收到消息

  * ![](/assets/当收到消息.png)

  * function chatReceiveHook\(str, sender\)

  * 参数

    * str : 消息内容

    * sender : 发送人

### 



