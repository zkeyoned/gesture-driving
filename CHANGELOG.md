# Changelog

## Gesture Drive v1.2 WIP - Background Image & Red Car Update

- 整理了 assets/backgrounds/ 目录
- 接入了 assets/backgrounds/cyber-highway-night.jpg 作为远景背景
- 保留了背景图加载失败时的 fallback
- 将车辆从暗色低模车调整为红色未来跑车方向
- 保留 HUD、摄像头窗口、右上状态面板
- 没有修改手势识别逻辑
- 没有修改车辆控制逻辑
- 当前仍待优化：车模型美观度、道路与背景融合、车辆与道路比例

## Gesture Drive v1.1.1 - Clean Visual Overlay Update

- 删除了画面里的斜向半透明虚线 / speed lines / motion streaks
- 保留 HUD、摄像头窗口、右上状态面板
- 保留刹车警示和基础 HUD 发光
- 没有修改手势识别逻辑
- 没有修改车辆控制逻辑
- 没有修改 MediaPipe 和 Three.js 主体

## Gesture Drive v1.1 - Stability & Cockpit HUD Update

- 修复 start() 重复启动问题
- 缓存 HUD / status DOM 查询
- 加入手势确认帧和短暂保持
- 加入转向 dead zone 和平滑插值
- 优化双手合十判断
- 初步升级 HUD、摄像头窗口和状态提示 UI
