# AI宠物狗狗安装指南

## 功能特点

1. **基础宠物互动**：喂食、玩耍、洗澡、睡觉、抚摸等基本互动
2. **技能训练系统**：训练宠物学习各种技能，提高等级
3. **成长系统**：宠物会随着时间成长，提升等级，解锁更多功能
4. **丰富的视觉效果**：基于宠物品种和性格的可视化表现
5. **环境互动**：天气系统、季节变化和玩具放置功能
6. **迷你游戏**：接飞盘等迷你游戏提供更多互动乐趣
7. **昼夜循环**：游戏内时间流逝，影响宠物状态和环境
8. **语音识别**：通过语音命令与宠物互动（需要浏览器支持）

## 系统要求
- Windows/macOS/Linux操作系统
- Python 3.6 或更高版本
- 显示器分辨率建议 1280x720 或更高

## 技术实现

- 桌面版：Python + Pygame
- Web版：
  - 后端：Python + Flask + Flask-SocketIO
  - 前端：HTML5 + CSS3 + JavaScript
  - 实时通信：WebSocket
  - 图形渲染：HTML5 Canvas

## 安装步骤

### 方法一：直接安装（推荐）

1. 确保你已安装Python 3.7或更高版本
   ```
   python --version
   ```

2. 克隆项目仓库
   ```
   git clone https://github.com/yourusername/ai_pet_dog.git
   cd ai_pet_dog
   ```

3. 安装依赖
   ```
   pip install -r requirements.txt
   ```

### 运行应用

#### 桌面版（Pygame界面）
```
python main.py
```

#### Web版（基于Flask）
```
python app.py
```
然后在浏览器中访问 http://localhost:5000/

## 项目结构

```
ai_pet_dog/
├── main.py          # 桌面版主程序入口
├── app.py           # Web版主程序入口
├── dog.py           # 宠物类定义
├── ui.py            # 桌面版用户界面
├── requirements.txt # 项目依赖
├── assets/          # 图像和音效资源
│   ├── images/      # 宠物和界面图像
│   │   ├── pixel_dogs/  # 宠物图像
│   │   ├── animations/  # 动画帧序列
│   │   ├── backgrounds/ # 背景场景
│   │   └── items/       # 互动物品图像
│   └── sounds/      # 游戏音效
├── minigames/       # 迷你游戏模块
│   ├── fetch.py     # 接飞盘游戏
│   ├── maze.py      # 迷宫游戏
│   └── race.py      # 障碍跑游戏
├── interaction/     # 交互功能模块
│   ├── voice.py     # 语音识别功能
│   ├── touch.py     # 触摸和手势识别
│   └── emotion.py   # 情感反馈系统
├── templates/       # Web版模板
│   └── index.html   # 主页面
├── static/          # Web版静态资源
│   └── game.js      # Web版游戏逻辑
└── data/            # 数据存储
    └── saves/       # 存档文件
        ├── dog.json  # 桌面版存档
        └── web/      # Web版存档
```

## 宠物创建与互动指南

### 创建宠物
可选择不同品种和性格组合：
- 品种：柯基、哈士奇、金毛、拉布拉多、柴犬
- 性格：活泼、温顺、机警、粘人、独立

每种组合会影响宠物的行为方式和属性变化。

### 基础互动指南
1. **喂食**：提供不同类型的食物，影响饥饿度和健康值
2. **玩耍**：提高快乐度，消耗能量
3. **洗澡**：提高清洁度
4. **睡觉**：恢复能量
5. **训练**：学习新技能或提升现有技能等级
6. **环境互动**：改变天气，放置玩具
7. **迷你游戏**：参与小游戏增加互动性

### 语音命令
支持以下语音命令（需浏览器支持WebSpeech API）：
- "喂食"/"吃饭"
- "玩耍"
- "洗澡"/"清洁"
- "睡觉"
- 技能名称如"坐下"、"握手"等

## 注意事项

1. 桌面版和Web版共享同一个核心宠物逻辑（dog.py），但数据存储在不同位置
2. 所有图像资源应放在assets目录下的适当子目录中
3. 如需添加新的狗狗品种或特性，可修改dog.py中的相关常量

## 开发扩展

### 添加新的迷你游戏
1. 在minigames目录下创建新的游戏文件
2. 在minigames/__init__.py中导出游戏类
3. 在main.py中集成新游戏

### 添加新的交互方式
1. 在interaction目录下创建新的交互文件
2. 在interaction/__init__.py中导出交互类
3. 在ui.py中集成新交互功能

## 常见问题

1. **提示"pygame module not found"**
   - 请确保已正确执行步骤3安装依赖
   - 尝试手动安装pygame：`pip install pygame`

2. **游戏窗口无法正常显示**
   - 确保你的显示器分辨率满足最低要求
   - 检查是否已安装最新的显卡驱动

3. **游戏无法启动**
   - 确保Python版本正确
   - 检查是否所有文件都已正确解压
   - 确保在正确的目录下运行命令

## 联系与支持

如果你在安装或运行过程中遇到任何问题，请：
1. 检查上述常见问题解决方案
2. 查看项目README.md文件获取更多信息

祝你玩得开心！
