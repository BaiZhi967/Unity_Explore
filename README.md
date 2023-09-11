# Unity_Explore

## 介绍
用来存放一些自己在学习Unity过程中做的测试demo功能

## Demo
### overcook-like

链接：https://github.com/BaiZhi967/overcook-like
简介：仿Overcook的联机游戏 一个学习多人游戏的练习项目 使用NetCode进行网络同步
用Unity复刻的Overcook，使用NetCode作为联机解决方案
状态同步+NetCode实现联机,使用Relay+Lobby提供匹配和连接服务设计和实现多人游戏大厅系统,包括玩家匹配和房间管理等功能
实现游戏中的物理和逻辑交互,拾取放置、碰撞检测、制作食物、完成订单、计算得分
借助InputSytem实现多设备绑定

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