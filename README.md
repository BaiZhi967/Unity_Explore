# Unity_Explore

## 介绍
记录自己学习Unity的经历

## Demo
### overcook-like

链接：https://github.com/BaiZhi967/overcook-like
简介：仿Overcook的联机游戏 一个学习多人游戏的练习项目 使用NetCode进行网络同步
用Unity复刻的Overcook，使用NetCode作为联机解决方案
状态同步+NetCode实现联机,使用Relay+Lobby提供匹配和连接服务设计和实现多人游戏大厅系统,包括玩家匹配和房间管理等功能
实现游戏中的物理和逻辑交互,拾取放置、碰撞检测、制作食物、完成订单、计算得分
借助InputSytem实现多设备绑定

### 2D模拟经营+RPG游戏 

**主要功能模块:背包商店系统，种植系统，建造系统，对话系统，任务系统，多进度通用存储系统、装备和技能系统** 
背包系统分离逻辑和数据,降低了模块间的耦合度和系统的通用性 
玩家信息、游戏进度、任务表、物品数据、装备技能信息等通过读取JSON文件和配置表实现自动生成和持久化 
通过有限状态机实现简单怪物的行为逻辑，以及自己编写的一个简易行为树框架实现复杂Boss的机制 
技能系统使用策略模式、将效果和表现进行分离，实现模块的解耦 
利用对象池管理特效，音效，游戏物体的创建和回收，通过观察者模式定义泛型的事件中心，提供事件监听和触发方法 
利用HybridCLR + Addressable实现资源和代码的热更新 

### 2D地下城RougeLike游戏

链接：https://github.com/BaiZhi967/DungeonRougeDemo

### 类星露谷物语模拟经营游戏

链接：https://github.com/BaiZhi967/MyFarmDemo

简介：2D像素模拟经营类游戏，有背包商店箱子系统，作物生长系统，建造系统，对话系统，多进度通用存储系统。数据存储：使用UI Toolkit配置、ScriptableObject存储物品数据，通过Json序列话和反序列化实现存档系统
核心系统：通过Tilemap实现地图信息系统，在此基础上实现了作物种植和建造系统，并将地图瓦片信息存储到ScriptableObject中
AStar寻路：通过Astar寻路算法自动计算NPC的行走路径，结合时间系统实现NPC的自动行走
利用对象池管理掉落物品，应用观察者模式，定义事件中心，提供事件的监听和触发的方法，通过BlendTree实现移动动画混合，使用Animator Override实现动画状态机复用

### 类杀戮尖塔的 CCG 卡牌游戏

链接：https://github.com/BaiZhi967/CardGameDemo

类杀戮尖塔的对战形式 + 类月圆之夜的关卡选择
实现了一套简易的框架，包括UI管理、资源管理、音频管理、事件中心和数据存储与加载。
根据MVC模式，所有面板由UIManager管理显示、隐藏、获取、添加自定义事件等，所有面板类拥有共同的UIBase基类，定义面板公有功能，获取所有UI控件并注册UI事件，方便子类使用
通过Excel表格导入卡牌、怪物和关卡信息，自动生成对于的游戏对象


## Framework

### WhiteZhiFramework

链接：https://github.com/BaiZhi967/WhiteZhiFramework

自己在开发过程中设计和整理的一套个人使用的小型游戏开发框架
符合 SOLID 原则、事件驱动、数据驱动、分层、MVC 、CQRS、模块化、易扩展的架构
框架还包括定时函数调用、对象池、音频和视频播放器、FSM、事件系统、场景加载器、UI管理器、单例和命令模式等多个实用工具;
加入了优先队列,树,BindableProperty等多个自定义数据类型
对Unity及C#中部分类型和方法的扩展，以及大量实用的静态方法


## Toolkits

### Simple Behavior Tree

链接：https://github.com/BaiZhi967/SimpleBehaviourTree

简介：这是一个简单的Unity的行为树插件。 其中使用了使用了Odin做可视化和UniTask插件实现异步操作 （需要自己导入插件）

实现了行为树种的基础节点功能

### Unity_Toolkit [弃用] 功能以整合进入 WhiteZhiFramework 中

链接：https://github.com/BaiZhi967/Unity-Toolkit/tree/master

简介：放一些自己平常开发过程中的工具