# 🏝️ Curl V1 — Dynamic Island for Windows 11

<p align="center">
  <img src="icon.png" width="96" height="96" alt="Curl Logo" />
</p>

<p align="center">
  <b>The world's most fluid, zero-lag Apple Dynamic Island experience for Windows 11</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-00F2FE?style=for-the-badge" alt="Version" />
  <img src="https://img.shields.io/badge/Platform-Windows%2011-0078D7?style=for-the-badge&logo=windows" alt="Platform" />
  <img src="https://img.shields.io/badge/Idle%20CPU-0.0%25-10B981?style=for-the-badge" alt="CPU" />
  <img src="https://img.shields.io/badge/RAM-~17MB-8B5CF6?style=for-the-badge" alt="RAM" />
  <img src="https://img.shields.io/badge/License-MIT-EC4899?style=for-the-badge" alt="License" />
</p>

---

## 🎬 Live Preview

https://github.com/user-attachments/assets/your-video-id

<!-- Or if the video is inside the repo: -->
<video src="Curl.mp4" width="100%" controls autoplay muted loop></video>

<p align="center"><i>Watch how notifications elastically drop, bloom, and tuck away with real iOS spring physics</i></p>

---

## ✨ Overview

**Curl** brings the signature Apple Dynamic Island to Windows 11 — beautifully.

Instead of ugly rectangular toast banners that block your screen, notifications elastically emerge from a sleek notch pill at the top of your display with authentic iOS spring physics, live app logos, and rich media previews.

Built from scratch with a **zero-lag architecture**, Curl uses event-driven SQLite WAL change tracking to achieve instantaneous notification rendering while consuming **0% idle CPU** and under **20 MB RAM**.

---

## 🚀 Key Features

- **🍏 Authentic 4-Phase Spring Physics**  
  Drops from the top bezel as a compact **74px notch pill** → dwells 700ms so you see the app logo → elastically blooms open with `cubic-bezier(0.16, 1, 0.3, 1)` → snaps back to compact pill → smoothly tucks away into the bezel.

- **⚡ 0% Idle CPU & Ultra-Lightweight**  
  Zero polling loops. Pure asynchronous Windows Push Notification SQLite database watcher with instant reaction time.

- **🛡️ 0ms Toast Deflector (Taskbar Auto-Hide Safe)**  
  Native background deflector prevents invisible Windows toast hit-test blocks. Your bottom-right auto-hide taskbar sensor stays 100% responsive.

- **💎 Dual Aesthetic Themes**  
  - **OLED Pitch Black** — Pure `#000000` with subtle neon cyan accents & inner glow  
  - **Frosted iOS Light** — 28px backdrop blur with true glassmorphism

- **📸 Rich Screenshot & Clipboard Previews**  
  Automatically captures Snipping Tool / Snip & Sketch screenshots and clipboard images and shows high-res previews inside the island.

- **🎯 Perfect App Logo Resolution**  
  Curated vector SVGs + sub-millisecond Windows shortcut icon resolution for Telegram, Chrome, WhatsApp, Discord, Spotify, and every desktop/UWP app.

- **⌨️ Instant Shortcut**  
  `Ctrl + Alt + C` — Open the settings dashboard anytime.

---

## 🎬 How It Works

```mermaid
graph TD
    A["App Sends Notification<br/>(Telegram, Chrome, etc.)"] --> B["Windows Push Notifications"]
    B --> C["wpndatabase.db WAL Event"]
    C --> D["Curl SQLite Watcher<br/>(0ms Capture)"]
    D --> E["Compact 74px Notch Pill Drops"]
    E -- 700ms Dwell --> F["Elastic Spring Bloom<br/>into Full Card"]
    F -- Reading Time --> G["Contract back to Pill"]
    G -- 700ms Dwell --> H["Smooth Tuck into Bezel"]
