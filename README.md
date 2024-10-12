# 关于这个项目
这仅是一个公布接口的仓库,项目内容不放于此.<br>
> 注意:请勿操作引擎资产内的`RZ`文件夹,谢谢.

# 从哪里开始
完整的运行需要进入关卡`Main`然后开始播放.

# 如何配置UMG层级显示
在引擎资产的根目录下有一个`ConfigData`文件,打开后可配置:<br>
![](https://github.com/dreamrz/Interface/blob/main/3.JPG)

### 内部数据说明
- `BigPlayerImageZOrder` 这是点击玩家头像后显示的层级<br>
![](https://github.com/dreamrz/Interface/blob/main/4.jpg)

- `Part1ZOrder` 这是调用globa widget part 1后的层级<br>
![](https://github.com/dreamrz/Interface/blob/main/5.jpg)

# 交互接口
### 关闭人物形象展示.
任意地方调用`globa close player figure`比如:<br>
![](https://github.com/dreamrz/Interface/blob/main/2.JPG)

### 相机从3D抬高到2D
任意地方调用`global change camera location`比如:<br>
![](https://github.com/dreamrz/Interface/blob/main/1.JPG)
> 建议调用前关闭人物形象展示.

### 抬高到2D后启动小地图预览UMG
任意地方调用`globa widget part 1`比如:<br>
![](https://github.com/dreamrz/Interface/blob/main/6.JPG)

# 对方的按钮或事件触发如何获取?
### 初始步骤
1. 引擎里菜单 `编辑` -> `项目设置` -> `地图和模式` -> `游戏实例类` 设置为 `DataGameInstance`
### 如何使用
1. 找到引擎资产的内容根目录下 `DataGameInstance` 蓝图,并打开.
2. 蓝图如下:<br>
![](https://github.com/dreamrz/Interface/blob/main/returnevent1.JPG)<br>
当被触发后会执行这里,将需要做的内容按需在后面进行编辑.(对方已不再编辑该蓝图,后续将由操作者自行编辑)

### 返回的事件 `点击人物后`
操作的界面:<br>
![](https://github.com/dreamrz/Interface/blob/main/button1.JPG)<br>

消息: `ClickPlayer`<br>
在`DataGameInstance` 蓝图中的switch string里加入`ClickPlayer`然后进行后续操作.
