# DrawAnythingToYakiji — 画什么都变成鸭吉吉

一个创意绘图网页应用，无论你在画布上画什么，它都会通过**粒子变形动画**将你的涂鸦变成可爱的**鸭吉吉**（鸭子/小鸡吉祥物）插画！

**在线体验：** [DrawAnythingToYakiji](https://tsanghaotian.github.io/DrawAnythingToYakiji/)

![演示](img/1.png)

## 玩法

1. **画画** — 在画布上用鼠标或手指随便画点什么
2. **停笔** — 停笔 1 秒后自动识别笔画
3. **变身** — 观看你的涂鸦通过粒子逐个飞散重组，变成一张鸭吉吉插画
4. **继续画** — 每次新笔画都会变成不同的鸭吉吉图片
5. **清空** — 点击按钮重新开始

## 功能亮点

- **粒子变形** — 每一笔都会分裂成数百个彩色粒子，再重新组合成目标图片
- **智能旋转** — 通过主成分分析（PCA）计算笔画角度，自动旋转目标图片匹配绘画方向
- **12 张不同鸭吉吉** — 每画一笔按顺序切换到下一张图片
- **移动端适配** — 完整支持触屏操作，画布自适应
- **零依赖** — 纯 HTML + CSS + JavaScript，无需任何框架或库

## 技术实现

- 纯 JS Canvas 渲染
- `requestAnimationFrame` 动画循环与缓动函数
- 主成分分析（PCA）计算笔画的主方向角度
- 源图像素采样，用于粒子颜色数据
- 兼容 `file://` 协议 — 在 CORS 限制下自动回退为网格采样

## 项目结构

```
├── index.html          # 主应用（单 HTML 文件）
├── img/                # 12 张鸭吉吉插画 PNG
│   ├── 1.png
│   ├── 2.png
│   └── ... up to 12.png
├── .github/workflows/  # GitHub Pages 自动部署
└── README.md
```

## 作者

由 [TsangHaotian](https://github.com/TsangHaotian) 创作
