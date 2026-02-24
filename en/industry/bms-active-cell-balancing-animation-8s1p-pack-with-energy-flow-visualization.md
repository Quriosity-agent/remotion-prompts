# BMS Active Cell Balancing Animation - 8S1P Pack with Energy Flow Visualization

**Likes:** 6
**Model:** Opus 4.6
**Tool:** Claude Code
**GitHub:** pasrom
**Date:** 2026-02-05T19:58:34.589Z

## Prompt

Create a Remotion project that renders a BMS Active Cell Balancing animation. 10 seconds, 30fps, 1280x720, output as MP4.                                                                                   
                                         
  Setup:                                                                                                                                                                                                      
  mkdir remotion-bms && cd remotion-bms                                                                                                                                                                       
  npm init -y                                                                                                                                                                                                 
  npm i remotion react react-dom                            
  npm i -D @remotion/cli typescript
  tsconfig.json: ES2022, jsx: react-jsx, moduleResolution: bundler, module: ESNext

  Project structure: src/index.ts, src/Root.tsx, src/BmsCellBalancing.tsx

  Animation (BmsCellBalancing.tsx):
  8 cells (8S1P) in a pack, dark theme (#0b1120), Courier New font. Initial voltages unbalanced between 3.3V and 4.05V. Background with subtle grid lines.

  Phases (at 300 frames total):
  - Frame 0..60: IDLE, show unbalanced cells
  - Frame 60..90: MEASURING CELLS... (yellow status dot)
  - Frame 90..240: BALANCING (green pulsing dot), voltages converge via smoothstep to average
  - Frame 240..300: BALANCED (blue)

  Each cell shows:
  - Color-coded SOC fill level (green when high, orange when medium, red when low) with gradient
  - Terminal nub on top, bus bars top/bottom connecting all cells
  - Voltage display (3 decimal places), cell label (C1..C8), SOC in %, temperature
  - During balancing: green border + arrow down for cells below avg (Charging), orange border + arrow up for cells above avg (Discharging)
  - Particle animation visualizing energy flow
  - Shimmer effect on the fill level

  Info panel at bottom with spring animation: Pack Voltage, Max Delta (color-coded: green below 10mV, orange below 50mV, red above), Avg Cell, Config (8S1P), Pack SOC, Method: Active

  Legend at bottom: "▲ Discharging (high cell)" orange, "▼ Charging (low cell)" green

  Render: npx remotion render src/index.ts BmsCellBalancing out/bms-cell-balancing.mp4
