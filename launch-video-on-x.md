# Launch Video on X

**Likes:** 48
**Model:** Opus 4.6
**Tool:** Claude code
**Author:** @ghumare64
**Date:** 2026-02-06T12:23:20.840Z

## Prompt

Create a Remotion video (1080x700, 30fps, ~37s) for OpenClawd â€” an open source AI desktop agent. Dark theme (#0c0a09
  background, #fbbf24 amber accent). Background music: "Walen - HEADPHONK" with 1s fade-in and 2s fade-out at 40% volume. 8
  scenes in series:

  Scene 1 â€” Terminal Install (120 frames / 4s)
  Mac-style terminal window with traffic light dots. Types npx openclawd-cli character by character (1 frame/char). After
  typing, shows ASCII art logo "OPENCLAWD" in amber, then server output lines appearing progressively: version banner, SDK
  backends, 20+ providers/80+ models loaded, model names (Opus 4.6, GPT-5.3, Gemini 3, etc.), MCP servers connected, "Opening
  desktop app on :3001". Terminal slides in from bottom with 3D perspective (rotateX 20deg, slight rotateY oscillation).

  Scene 2 â€” Home Screen (150 frames / 5s)
  Desktop app window with centered "OpenClawd" title (Georgia serif), tagline "Open Source Alternative to Claude Cowork",
  rounded chat input with send button, and provider/model selector chips (Claude Code + Opus 4.6 + Attach). Spring-animated
  fade-in with staggered delays (title â†’ tagline â†’ input â†’ controls).

  Scene 3 â€” Chat Interface (160 frames / 5.3s)
  Three-column layout: left sidebar with chat history (MCP Integration, Code Review, etc.), center with user message "Review my
   API code" and streaming assistant response about security findings (rate limiting, SQL injection, input validation), right
  panel showing progress steps (Reading â†’ Security analysis â†’ Applying fixes â†’ Creating PR) and tool calls (filesystem.read,
  bash.exec, github.create_pr) with green checkmarks.

  Scene 4 â€” Provider Switch (130 frames / 4.3s)
  Two dropdown panels side by side. Left: 8 providers (Claude Code, OpenCode, OpenAI, Gemini, DeepSeek, Llama 4, MiniMax,
  Ollama) with colored dots and selection indicator. Right: 7 models (Opus 4.6, Sonnet 4.5, GPT-5.3 Codex, etc.) with
  descriptions. Bottom tagline: "Claude Code + OpenCode SDK â€” 20+ providers Â· Open Source models". Staggered item reveals.

  Scene 5 â€” MCP Catalog (140 frames / 4.7s)
  Modal overlay with "MCP Server Catalog â€” 20+ servers available". Category filter pills (All, Core, Database, Developer,
  Communication). 6 server cards with icons: Filesystem, Git, GitHub (installed), PostgreSQL, Slack, Puppeteer. Auth badges
  (green "No Auth" / amber "Requires Auth"). Install/Installed buttons with checkmarks.

  Scene 6 â€” Messaging Bots (120 frames / 4s)
  Full-screen "Your AI, everywhere you chat" with subtitle "Full tool access Â· Memory Â· Scheduling". 4 platform cards
  (WhatsApp, Telegram, Signal, iMessage) with SVG icons, green "Connected" status dots, and feature tags (Memory, Scheduling,
  Tools). Cards scale up with spring animation.

  Scene 7 â€” Logo Combo (180 frames / 6s)
  Three sub-scenes: (a) Intro with converging amber lines, center burst ring, floating particles, grid background. (b) "âœ¦
  Introducing âœ¦" with word-by-word reveal: "Open Source AI Desktop" in 56px white text, model names below in gray monospace.
  (c) 8 provider icons in two rows with colored dots and labels, tagline "Claude Code + OpenCode SDK Â· 80+ models | Desktop Â·
  Messaging Â· API".

  Scene 8 â€” GitHub CTA (120 frames / 4s)
  "100% OPEN SOURCE" label, spinning GitHub logo (rotates in from -180deg), orbiting amber star icons, "Star us on GitHub" in
  36px white, pulsing scale animation, "github.com/rohitg00/openclawd" in monospace with dark card background. Floating
  particles and subtle grid.

  All transitions use spring animations with fade + scale (0.95â†’1 in, 1â†’0.95 out). Each scene inside an AppWindow component
  (mac chrome with traffic lights). Color palette: #0c0a09 bg, #1c1917 surfaces, #292524 borders, #fbbf24 amber accent, #fafaf9
   white text, #a8a29e muted text, #78716c dim text. Fonts: Inter for UI, SF Mono for code, Georgia for branding.

