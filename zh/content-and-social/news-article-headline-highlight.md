# 新闻文章标题高亮

**点赞:** 70
**模型:** Claude Code
**工具:** Opus 4.5
**作者:** @Remotion
**日期:** 2026-02-01T10:55:20.520Z

## 提示词

使用 remotion best practices。将以下图片导入项目：'~/Desktop/Screenshot 2026-01-31 at 17.15.12.png'，使用 tesseract CLI 进行 OCR 识别文字位置。在 Remotion 中，创建一个新的 Composition，加载图片并在全高清白色背景上为文章留出充裕的内边距。Composition 运行 5 秒期间，缓慢且非常微妙地放大，同时将文章从左到右进行轻微的 3D 旋转。每个轴的整体旋转约为 15 度。开始时模糊整个 Composition，在 1 秒内取消模糊。模糊完成后，使用 rough.js 在 "government shutdown" 和 "funding lapses" 上方从左到右展开荧光笔效果。图片有白色背景。确保标记出现在文字后面。安装新依赖时，检查现有的 lockfile 并使用正确的包管理器。