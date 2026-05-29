# Gesture Drive

## 项目简介

Gesture Drive 是一个基于摄像头手势识别的网页驾驶小游戏。用户可以先在 Gesture Garage 车库里选择车辆，再通过手部动作控制汽车，在 Three.js 驾驶场景中完成油门、刹车、急刹和转向操作。

## 当前版本

Gesture Drive v1.2 - Gesture Garage & GLB Vehicle Selection

当前版本加入了轻量版手势车库：

- 进入页面后先显示 Gesture Garage 车辆选择界面
- 支持左右挥手切换车辆
- 支持握拳保持 2 秒进入 READY TO DRIVE 确认状态并自动启动驾驶
- 保留鼠标 / 触控备用操作
- 点击 START DRIVE / INITIATE DRIVE 后加载选中的 GLB 车辆
- GLB 加载失败时不会进入驾驶，会在车库界面提示错误

## 当前可选车辆

当前车库选择列表只保留了测试中可见性较好的 4 个模型：

| 名称 | 文件 | 标签 |
| --- | --- | --- |
| Crimson GT | `assets/models/car-01.glb` | Balanced |
| Street Phantom | `assets/models/car-04.glb` | Agile |
| Velocity RS | `assets/models/car-05.glb` | Speed |
| Cyber Runner | `assets/models/car-06.glb` | Future |

`car-02.glb` 和 `car-03.glb` 仍保留在 `assets/models/` 中，但因为驾驶视角下过暗 / 不明显，暂时不放入车库选择列表。

## 主要功能

- Gesture Garage 手势选车
- 右手拇指控制油门
- 左手拇指控制轻刹
- 双手合十触发急刹
- 双手倾斜控制转向
- Three.js 驾驶场景
- Three.js GLTFLoader 车辆模型加载
- MediaPipe Hands 手势识别
- 摄像头辅助窗口
- 驾驶舱 HUD

## 如何运行

必须通过本地服务器运行项目，不要直接双击 `index.html`。

推荐命令：

```bash
python3 -m http.server 8000
```

然后打开：

```text
http://localhost:8000/index.html
```

浏览器需要允许摄像头权限。推荐使用 Chrome 浏览器。

## 操作方式

| 场景 | 手势 / 操作 | 功能 |
| --- | --- | --- |
| 车库 | 左右挥手 | 切换车辆 |
| 车库 | 握拳保持 2 秒 | 确认当前车辆并自动启动驾驶 |
| 车库 | 点击左右箭头 / 车辆卡片 | 备用切换 / 确认 |
| 车库 | 点击 START DRIVE / INITIATE DRIVE | 进入驾驶 |
| 驾驶 | 右手拇指动作 | 油门 |
| 驾驶 | 左手拇指动作 | 轻刹 |
| 驾驶 | 双手合十 | 急刹 |
| 驾驶 | 双手向左 / 向右倾斜 | 转向 |

## 文件结构

```text
assets/
  backgrounds/
    cyber-highway-night.jpg
  models/
    car-01.glb
    car-02.glb
    car-03.glb
    car-04.glb
    car-05.glb
    car-06.glb
```

项目仍保持单文件应用结构，主程序在 `index.html`。

## 版本备份文件

- `index-v1.2-bg-redcar-wip.html`：v1.2 背景图和红色几何体车阶段备份
- `index-v1.2-pre-glb-model-test.html`：接入 GLB 模型前备份
- `index-v1.2-pre-gesture-garage.html`：Gesture Garage UI 前备份

## 后续优化方向

- 用真实 GLB 预览替换车库里的示意车图
- 继续筛选更适合尾视角的车辆模型
- 优化车库视觉表现
- 优化近景道路与远景背景融合
- 更强的速度感
- 手势校准页面
