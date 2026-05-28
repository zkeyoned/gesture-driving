# Changelog

## Gesture Drive v1.2 - Gesture Garage & GLB Vehicle Selection

- 新增 Gesture Garage 车库选择界面
- 新增左右挥手切换车辆
- 新增双手张开确认车辆，进入 READY TO DRIVE 状态
- 保留鼠标 / 触控备用操作：左右箭头、车辆卡片、START DRIVE 按钮
- 接入 Three.js GLTFLoader，通过 `assets/models/${selectedCarModel.file}` 加载当前选中车辆
- 启动驾驶前会清空旧车辆对象，避免多个模型叠加或残留旧车
- GLB 加载成功时输出 `Selected car`、`Loading GLB car`、`GLB car loaded` 和 `car.children` 调试信息
- GLB 加载失败时不再进入驾驶画面，避免误显示 fallback 红色几何体车
- 保留 `car` 作为车辆父级 Group，驾驶循环中的 `car.position.x` 和 `car.rotation.y` 继续正常工作
- 保留驾驶 HUD、摄像头窗口、右上状态面板、MediaPipe 初始化和驾驶手势核心逻辑
- 将 `car-04.glb`、`car-05.glb`、`car-06.glb` 标准化放入 `assets/models/`
- 暂时从车库选择列表移除驾驶视角下可见性较差的 `car-02.glb` 和 `car-03.glb`
- 修正 `car-05.glb` 的尾视角朝向

## Gesture Drive v1.2 WIP - Background Image & Red Car Update

- 整理了 `assets/backgrounds/` 目录
- 接入了 `assets/backgrounds/cyber-highway-night.jpg` 作为远景背景
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
