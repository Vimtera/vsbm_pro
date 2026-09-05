# vsbm_pro
[中文](#zh) | [English](#en)

# 🍄 毒蘑菇 · GPU 性能测试 (vsbm_pro)

> 一个基于 WebGL 体积着色器的实时 GPU 压力测试工具，集成 FPS 监测、性能曲线、设备信息与数据导出功能。  
> 可自由拖拽视角、缩放，直观评估设备图形渲染性能。

---

## <a id="zh">🇨🇳 中文版</a>

### ✨ 功能特性

- 🎨 **实时 3D 体积着色器** – 基于三角函数与迭代算法生成绚丽的"毒蘑菇"效果，持续压榨 GPU 性能  
- 📊 **实时性能监测** – 显示当前帧率 (FPS)、平均帧率、最低帧率，并动态着色反馈  
- 📈 **FPS 走势曲线** – 绘制最近 240 个采样点的帧率变化，附带 60fps 参考线  
- 🖥️ **设备信息展示** – 自动识别浏览器、操作系统、GPU 型号、CPU 核心数、内存与屏幕分辨率  
- 💾 **一键导出数据** – 将帧率历史、统计摘要和设备信息导出为 CSV 文件，便于后续分析  
- ⚙️ **自定义着色器** – 支持实时编辑并应用片段着色器内核，调整计算复杂度以适配不同测试需求  
- 📱 **响应式交互** – 支持鼠标/触摸拖拽旋转、滚轮/双指缩放，适配移动端与桌面端  

### 🚀 快速开始

**在线体验**  
直接打开 [https://vimtera.github.io/vsbm_pro/](https://vimtera.github.io/vsbm_pro/) 或下载 `index.html` 在浏览器中运行即可。

**本地运行**  
1. 克隆仓库或下载 `index.html` 文件  
2. 在浏览器中打开该文件(推荐 Chrome / Edge / Firefox)  
3. 页面加载后自动开始渲染与性能监测

**交互操作**  
| 操作 | 效果 |
|------|------|
| 鼠标拖拽 / 单指滑动 | 旋转视角 |
| 鼠标滚轮 / 双指捏合 | 缩放画面 |
| 鼠标右键拖拽 / 双指平移 | 平移场景 |
| 点击 ⚙ CONFIG | 编辑着色器内核并应用 |

### 📦 导出数据说明

点击底部面板的 **"📥 导出数据"** 按钮，会生成一个 CSV 文件，包含以下内容：

- 头部注释：导出时间、设备信息(浏览器 / OS / GPU / CPU / 内存 / 屏幕)  
- 统计摘要：总采样帧数、平均 FPS、最低 FPS、最高 FPS  
- 数据列表：以 `帧序号, FPS` 格式记录的每一帧采样值(采样间隔约 500ms)

该 CSV 可直接用 Excel、Numbers 或文本编辑器打开，便于制作图表或进行性能对比分析。

### 🛠️ 技术栈

- **WebGL** – 渲染体积着色器  
- **Canvas 2D** – 绘制 FPS 曲线  
- **原生 JavaScript** – 无第三方依赖  
- **HTML5 + CSS3** – 响应式界面与毛玻璃效果

### 📁 文件结构

```

.
├── index.html       # 单页应用，包含所有 HTML / CSS / JS
└── README.md        # 项目说明

```

### ✏️ 自定义着色器

点击 `CONFIG` 按钮可以编辑 `kernal(vec3 ver)` 函数，该函数定义了体积场的形状与颜色。  
修改后点击 `APPLY` 即可实时生效，方便测试不同复杂度的着色器对性能的影响。

默认内核使用三角函数迭代生成螺旋状结构，你可以在 `KERNEL` 变量中替换为自己的算法。

### 🤝 贡献

欢迎提交 Issue 或 Pull Request。  
如果你有改进建议、新功能想法或报告 Bug，请随时参与。

### 📄 许可证

本项目采用 **MIT License** 开源，可自由使用、修改和分发。

### 🙏 致谢

- 原始体积着色器灵感来自 [cznull@bilibili](https://space.bilibili.com/) 的 `volumeshader_bm` 示例  
- 感谢所有开源社区的贡献者

---

## <a id="en">🇬🇧 English Version</a>

### ✨ Features

- 🎨 **Real-time 3D Volume Shader** – Generates a gorgeous "poisonous mushroom" effect using trigonometric functions and iterative algorithms, continuously stressing your GPU.  
- 📊 **Real-time Performance Monitor** – Displays current FPS, average FPS, and minimum FPS with dynamic color feedback.  
- 📈 **FPS Trend Chart** – Plots the last 240 sample points with a 60fps reference line.  
- 🖥️ **Device Info Display** – Automatically detects browser, OS, GPU model, CPU cores, memory, and screen resolution.  
- 💾 **One‑Click Data Export** – Exports FPS history, statistics summary, and device info as a CSV file for further analysis.  
- ⚙️ **Customizable Shader** – Edit and apply the fragment shader kernel in real time to adjust computational complexity for different testing needs.  
- 📱 **Responsive Interaction** – Supports mouse/touch drag to rotate, scroll/pinch to zoom, and adapts to mobile and desktop devices.

### 🚀 Quick Start

**Online Demo**  
Open [https://vimtera.github.io/vsbm_pro/](https://vimtera.github.io/vsbm_pro/) directly, or download `index.html` and run it in your browser.

**Run Locally**  
1. Clone the repository or download the `index.html` file.  
2. Open the file in your browser (Chrome / Edge / Firefox recommended).  
3. The page will automatically start rendering and performance monitoring.

**Interaction Controls**  
| Action | Effect |
|--------|--------|
| Mouse drag / single‑finger swipe | Rotate view |
| Mouse scroll / two‑finger pinch | Zoom in/out |
| Right‑click drag / two‑finger pan | Pan scene |
| Click ⚙ CONFIG | Edit and apply shader kernel |

### 📦 Export Data Description

Click the **"📥 导出数据"** button at the bottom panel to generate a CSV file containing:

- Header comments: export time, device info (browser / OS / GPU / CPU / memory / screen)  
- Statistics summary: total frames, average FPS, minimum FPS, maximum FPS  
- Data list: each frame sample in `frame_number, FPS` format (sampling interval ~500ms)

The CSV can be opened with Excel, Numbers, or any text editor for charting or performance comparison.

### 🛠️ Tech Stack

- **WebGL** – Renders the volume shader  
- **Canvas 2D** – Draws the FPS curve  
- **Vanilla JavaScript** – No third‑party dependencies  
- **HTML5 + CSS3** – Responsive UI with glass‑morphism effects

### 📁 File Structure

```

.
├── index.html       # Single‑page app containing all HTML / CSS / JS
└── README.md        # Project documentation

```

### ✏️ Custom Shader

Click the `CONFIG` button to edit the `kernal(vec3 ver)` function, which defines the shape and color of the volume field.  
After modification, click `APPLY` to see the effect immediately, allowing you to test how different shader complexities impact performance.

The default kernel uses trigonometric iterations to generate a spiral structure. You can replace it with your own algorithm in the `KERNEL` variable.

### 🤝 Contributing

Issues and Pull Requests are welcome.  
Feel free to share improvement suggestions, new feature ideas, or bug reports.

### 📄 License

This project is open‑sourced under the **MIT License** – you are free to use, modify, and distribute it.

### 🙏 Acknowledgements

- Original volume shader inspired by [cznull@bilibili](https://space.bilibili.com/)'s `volumeshader_bm` example.  
- Thanks to all contributors in the open‑source community.

---

**Enjoy testing your GPU! 🍄**
```

---
