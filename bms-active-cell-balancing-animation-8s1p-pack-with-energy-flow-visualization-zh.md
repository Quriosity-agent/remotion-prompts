# BMS 主动电池均衡动画 - 8S1P 电池组能量流可视化

**点赞:** 6
**模型:** Opus 4.6
**工具:** Claude Code
**GitHub:** pasrom
**日期:** 2026-02-05T19:58:34.589Z

## 提示词

创建一个 Remotion 项目，渲染 BMS 主动电池均衡动画。10 秒，30fps，1280x720，输出为 MP4。

设置：
mkdir remotion-bms && cd remotion-bms
npm init -y
npm i remotion react react-dom
npm i -D @remotion/cli typescript
tsconfig.json: ES2022, jsx: react-jsx, moduleResolution: bundler, module: ESNext

项目结构：src/index.ts, src/Root.tsx, src/BmsCellBalancing.tsx

动画（BmsCellBalancing.tsx）：
8 个电芯（8S1P）组成电池组，暗色主题（#0b1120），Courier New 字体。初始电压不平衡，范围在 3.3V 到 4.05V 之间。背景带微妙网格线。

阶段（共 300 帧）：
- 第 0..60 帧：空闲状态，显示不平衡的电芯
- 第 60..90 帧：测量电芯中...（黄色状态点）
- 第 90..240 帧：均衡中（绿色脉冲点），电压通过 smoothstep 收敛到平均值
- 第 240..300 帧：已均衡（蓝色）

每个电芯显示：
- 按 SOC 充电量着色的填充级别（高为绿色，中为橙色，低为红色）带渐变
- 顶部端子凸起，顶部/底部母线连接所有电芯
- 电压显示（3 位小数）、电芯标签（C1..C8）、SOC 百分比、温度
- 均衡期间：低于平均值的电芯显示绿色边框 + 向下箭头（充电中），高于平均值的显示橙色边框 + 向上箭头（放电中）
- 粒子动画可视化能量流
- 填充级别上的微光效果

底部信息面板带 Spring 动画：电池组电压、最大差值（颜色编码：低于 10mV 绿色，低于 50mV 橙色，高于则红色）、平均电芯、配置（8S1P）、电池组 SOC、方法：主动均衡

底部图例："▲ 放电中（高电压电芯）"橙色，"▼ 充电中（低电压电芯）"绿色

渲染：npx remotion render src/index.ts BmsCellBalancing out/bms-cell-balancing.mp4