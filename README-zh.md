# Remotion 提示词画廊 🎬

精选 21 个来自 [remotion.dev/prompts](https://www.remotion.dev/prompts) 的视频提示词 — 真实的 AI 生成视频案例，使用 [Remotion](https://remotion.dev) + AI 编程助手制作。

## 这是什么？

这些是真实用户使用 AI 编程助手（Claude Code、Cursor、Gemini、OpenCode）配合 Remotion 生成专业视频的提示词。可以作为灵感来源或项目模板。

## 热门提示词排行

| # | 提示词 | 点赞 | 模型 | 工具 |
|---|--------|------|------|------|
| 1 | [3D 地标旅行路线地图](zh/maps-and-data/travel-route-on-map-with-3d-landmarks.md) | 73 | Opus 4.5 | Claude Code |
| 2 | [新闻标题高亮动画](zh/content-and-social/news-article-headline-highlight.md) | 70 | Claude Code | Opus 4.5 |
| 3 | [X 平台发布视频](zh/product-and-marketing/launch-video-on-x.md) | 48 | Opus 4.6 | Claude Code |
| 4 | [Presscut 产品演示](zh/product-and-marketing/product-demo-for-presscut.md) | 40 | Claude Opus 4.5 | Claude Code |
| 5 | [火箭发射时间线](zh/maps-and-data/rocket-launches-timeline.md) | 36 | — | — |

## 分类

**🗺️ 地图与数据可视化**
- [旅行路线地图](zh/maps-and-data/travel-route-on-map-with-3d-landmarks.md) — 从洛杉矶到纽约再到巴黎的 3D 动画
- [火箭发射时间线](zh/maps-and-data/rocket-launches-timeline.md) — SpaceX 2015-2025 发射轨迹
- [柱状+折线混合图](zh/maps-and-data/bar-line-chart-combined.md) — 销售数据动画
- [游戏销量 Top 20](zh/maps-and-data/threejs-top-20-games-sold-ranking-1.md) — Three.js 3D 排行榜

**🎬 产品与营销**
- [X 平台发布视频](zh/product-and-marketing/launch-video-on-x.md) — OpenClaw 产品宣传片
- [Presscut 产品演示](zh/product-and-marketing/product-demo-for-presscut.md) — 创始人风格产品演示
- [VVTerm 推广视频](zh/product-and-marketing/promotion-video-for-vvterm.md) — 苹果风格宣传
- [唱片店促销](zh/product-and-marketing/music-cd-store-promo.md) — 音频响应式促销视频
- [动感营销视频](zh/product-and-marketing/the-kinetic-marketing.md) — 动态排版效果

**🎨 动效与 3D**
- [3D 旋转 Logo](zh/motion-graphics-and-3d/spinning-glitching-svg-logo-turned-3d.md) — 金属质感 + 故障效果
- [电影感人物介绍](zh/motion-graphics-and-3d/cinematic-tech-intro.md) — Jensen Huang 赛博朋克风
- [形状变文字](zh/motion-graphics-and-3d/shape-to-words-transformation.md) — 几何图形变形动画
- [3D 像素字体](zh/motion-graphics-and-3d/3d-retro-pixel-font.md) — 多光标协作像素构建

**📰 内容与社交**
- [新闻标题高亮](zh/content-and-social/news-article-headline-highlight.md) — OCR 识别 + 荧光笔效果
- [透明订阅按钮](zh/content-and-social/transparent-call-to-action-overlay.md) — YouTube 下方弹出动画
- [Strava 跑步可视化](zh/content-and-social/strava-run-visualized.md) — GPS 数据转 Instagram Story

**🏠 行业应用**
- [房地产投资视频](zh/industry/real-estate-investing.md) — 豪华房产宣传
- [电池管理系统动画](zh/industry/bms-active-cell-balancing-animation-8s1p-pack-with-energy-flow-visualization.md) — 技术可视化

**🎵 音频**
- [音频频谱可视化](zh/audio/audio-spectrum-visualizer.md) — 音乐频谱柱状图

**📢 公告**
- [Cursor Agent Skills 发布](zh/product-and-marketing/cursor-agent-skills-announcement.md) — 打字机效果公告视频
- [历史记录](zh/maps-and-data/history.md) — 柱状折线组合图表（含代码）

## 使用方法

1. 选一个你喜欢的提示词
2. 打开你的 Remotion 项目
3. 用 AI 编程助手运行：
   ```
   claude -p "<粘贴提示词>" --dangerously-skip-permissions
   ```
4. 自定义和迭代！

**中文用户小贴士：**
- 提示词可以用中文写，AI 会理解
- 中文字幕记得指定字体：`Noto Sans SC`（思源黑体）
- 竖屏抖音/小红书用 `1080x1920`，横屏用 `1920x1080`

## 文件说明

- `data/all-prompts.json` — 完整原始数据
- `*-zh.md` — 每个提示词的中文翻译文件（含元数据）
- `*.md` — 每个提示词的英文原始文件

## 来源

所有提示词于 2026-02-25 从 [remotion.dev/prompts](https://www.remotion.dev/prompts) 抓取。

---

[English →](README.md)