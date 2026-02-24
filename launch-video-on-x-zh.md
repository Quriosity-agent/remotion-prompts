# X 平台发布视频

**点赞:** 48
**模型:** Opus 4.6
**工具:** Claude Code
**作者:** @ghumare64
**日期:** 2026-02-06T12:23:20.840Z

## 提示词

创建一个 Remotion 视频（1080x700，30fps，约 37 秒），用于 OpenClawd — 一个开源 AI 桌面代理。暗色主题（#0c0a09 背景，#fbbf24 琥珀色强调色）。背景音乐："Walen - HEADPHONK"，1 秒淡入和 2 秒淡出，40% 音量。8 个连续场景：

场景 1 — 终端安装（120 帧 / 4 秒）
Mac 风格终端窗口，带交通灯圆点。逐字符打出 npx openclawd-cli（每帧 1 个字符）。打字完成后，显示琥珀色 ASCII 艺术 logo "OPENCLAWD"，然后逐行显示服务器输出：版本横幅、SDK 后端、20+ 提供商/80+ 模型已加载、模型名称（Opus 4.6、GPT-5.3、Gemini 3 等）、MCP 服务器已连接、"Opening desktop app on :3001"。终端从底部滑入，带 3D 透视效果（rotateX 20deg，轻微 rotateY 摆动）。

场景 2 — 主屏幕（150 帧 / 5 秒）
桌面应用窗口，居中显示 "OpenClawd" 标题（Georgia 衬线字体），标语 "Open Source Alternative to Claude Cowork"，圆角聊天输入框带发送按钮，以及提供商/模型选择器标签（Claude Code + Opus 4.6 + Attach）。Spring 动画淡入，带交错延迟（标题 → 标语 → 输入框 → 控件）。

场景 3 — 聊天界面（160 帧 / 5.3 秒）
三栏布局：左侧边栏显示聊天历史（MCP 集成、代码审查等），中间显示用户消息 "Review my API code" 和流式助手回复（关于安全发现：速率限制、SQL 注入、输入验证），右侧面板显示进度步骤（读取 → 安全分析 → 应用修复 → 创建 PR）和工具调用（filesystem.read、bash.exec、github.create_pr）带绿色对勾。

场景 4 — 提供商切换（130 帧 / 4.3 秒）
两个并排的下拉面板。左侧：8 个提供商（Claude Code、OpenCode、OpenAI、Gemini、DeepSeek、Llama 4、MiniMax、Ollama），带彩色圆点和选中指示器。右侧：7 个模型（Opus 4.6、Sonnet 4.5、GPT-5.3 Codex 等），带描述。底部标语："Claude Code + OpenCode SDK — 20+ providers · Open Source models"。交错项目展示。

场景 5 — MCP 目录（140 帧 / 4.7 秒）
模态弹窗显示 "MCP Server Catalog — 20+ servers available"。分类筛选标签（全部、核心、数据库、开发者、通信）。6 张服务器卡片带图标：Filesystem、Git、GitHub（已安装）、PostgreSQL、Slack、Puppeteer。认证徽章（绿色 "No Auth" / 琥珀色 "Requires Auth"）。安装/已安装按钮带对勾。

场景 6 — 消息机器人（120 帧 / 4 秒）
全屏显示 "Your AI, everywhere you chat"，副标题 "Full tool access · Memory · Scheduling"。4 张平台卡片（WhatsApp、Telegram、Signal、iMessage），带 SVG 图标、绿色 "Connected" 状态点和功能标签（Memory、Scheduling、Tools）。卡片带 Spring 动画放大。

场景 7 — Logo 组合（180 帧 / 6 秒）
三个子场景：(a) 前奏：汇聚的琥珀色线条、中心爆发光环、悬浮粒子、网格背景。(b) "✦ Introducing ✦" 逐词揭示："Open Source AI Desktop" 白色 56px 文字，下方灰色等宽字体显示模型名称。(c) 8 个提供商图标分两行排列，带彩色圆点和标签，标语 "Claude Code + OpenCode SDK · 80+ models | Desktop · Messaging · API"。

场景 8 — GitHub 行动号召（120 帧 / 4 秒）
"100% OPEN SOURCE" 标签，旋转的 GitHub logo（从 -180deg 旋转入场），环绕的琥珀色星形图标，"Star us on GitHub" 白色 36px 文字，脉冲缩放动画，"github.com/rohitg00/openclawd" 等宽字体暗色卡片背景。悬浮粒子和微妙网格。

所有过渡使用 Spring 动画，带淡入淡出 + 缩放（进入 0.95→1，退出 1→0.95）。每个场景在 AppWindow 组件内（Mac 窗口装饰带交通灯）。配色方案：#0c0a09 背景、#1c1917 表面、#292524 边框、#fbbf24 琥珀色强调、#fafaf9 白色文字、#a8a29e 柔和文字、#78716c 暗淡文字。字体：Inter 用于 UI、SF Mono 用于代码、Georgia 用于品牌。