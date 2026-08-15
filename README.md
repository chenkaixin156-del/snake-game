# 🐋 DeepSeek 贪吃蛇（Snake Game）

一个纯 HTML/CSS/JavaScript 实现的深海主题贪吃蛇小游戏，**零依赖、零构建**，双击 `index.html` 即可游玩。

## 🕹️ 在线试玩

**[https://chenkaixin156-del.github.io/snake-game/](https://chenkaixin156-del.github.io/snake-game/)**

## ✨ 特性

- **丝滑画面**：60fps 逐帧插值渲染 + smoothstep 缓动，蛇身为连续圆滑曲线，转弯不生硬
- **🐋 DeepSeek 蓝深海主题**：丁达尔光柱、漂浮气泡、鲸鱼水印、发光的深海珍珠
- **🧱 穿墙模式**：按 `C` 切换，带传送门特效；穿墙处断开连线 + 另一侧"传送镜像"，动画完全连续无卡顿
- **🎵 背景音乐**：WebAudio 实时合成的轻松活跃小曲（C–Am–F–G 进行，104 BPM），`M` 键开关
- **✨ 特效**：吃到珍珠气泡爆裂 + "+10" 飘字粒子系统
- **🏆 最高分本地记忆**（localStorage，刷新不丢失）
- **📱 响应式布局**：手机端虚拟方向键 + 触屏滑动，高 DPI 屏幕自适应清晰
- **🔊 合成音效**：吃食物 / 开始 / 结束均有提示音

## 🎮 操作

| 按键 | 功能 |
| --- | --- |
| `↑` `↓` `←` `→` / `W` `A` `S` `D` | 移动 |
| `空格` | 暂停 / 继续 |
| `R` | 重新开始 |
| `C` | 穿墙模式开关 |
| `M` | 背景音乐开关 |

## 🚀 本地运行

直接用浏览器打开 `index.html`，或：

```bash
npx serve snake-game
```

## 🛠️ 技术说明

- 纯原生 HTML / CSS / JavaScript，无任何外部依赖
- Canvas 2D + `devicePixelRatio` 适配，穿墙采用环面拓扑插值（最短路径渲染）
- WebAudio API 实时合成音效与背景音乐（振荡器 + 噪声 + 回声延迟链）
- 高分、穿墙模式、音乐开关均通过 localStorage 持久化
