# vibe-coding

> 用提示词驱动的交互式网页作品集：三个项目均为**单 HTML 文件、零构建、浏览器直接运行**。

| 项目 | 简介 | 技术 |
| --- | --- | --- |
| [Tidehaven](./tidehaven/) | 交互式 3D 海岸小岛立体模型：皮划艇、潜水、鳐鱼跳跃，潮汐 / 风 / 时间控制，日落亮灯 | Three.js · WebGL · Web Audio |
| [V8 Engine · Mechanical Atlas](./v8-engine/) | 高度细节化的 V8 发动机交互可视化：剖视 / 爆炸视图、零件标注、点火顺序与四冲程循环 | Three.js · WebGL · 程序化建模 |
| [one-form](./one-form/) | 单一形状在 12 种 UI 状态间连续形变的弹簧动画短片，120 BPM、无缝循环 | 原生 JS · 闭式弹簧物理 · Playwright / FFmpeg 渲染 |

## 共同特点

- **单文件交付**：每个项目只有一个 `index.html`，依赖库内联，双击即可运行
- **无框架、无构建**：原生 HTML / CSS / JavaScript，不依赖 npm 或打包工具
- **提示词驱动创作**：每个项目的 README 均按「原始提示词 → 效果图 → 技术栈」组织，完整记录从一句话到成品的过程
- **确定性渲染管线**：通过 Playwright 劫持 `requestAnimationFrame`、以虚拟时钟逐帧捕获，FFmpeg（h264_nvenc）硬件编码演示视频

## 目录结构

```
vibe-coding/
├── tidehaven/
│   ├── index.html
│   ├── README.md
│   └── screenshots/
├── v8-engine/
│   ├── index.html
│   ├── README.md
│   └── screenshots/
└── one-form/
    ├── index.html
    ├── README.md
    └── screenshots/
```

## 本地运行

进入任一项目目录，用浏览器打开 `index.html`，或使用静态服务器：

```bash
python -m http.server 8000
# 或
npx serve .
```

## License

代码均以 [MIT License](./LICENSE) 发布；第三方库（Three.js）、字体（Geist）与音乐（Mixkit）遵循各自原有许可。
