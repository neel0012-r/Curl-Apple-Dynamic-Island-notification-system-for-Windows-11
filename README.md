# 🏝️ Curl V1 — Dynamic Island for Windows 11

<p align="center">
  <b>A fluid Dynamic Island-style notification experience for Windows 11.</b>
</p>

---

## ✨ Overview

**Curl** brings a Dynamic Island-inspired notification experience to Windows 11.

Instead of traditional rectangular Windows notifications appearing in the bottom-right corner, Curl transforms notifications into a sleek, animated island at the top of the screen.

The island starts as a compact pill, expands smoothly into a notification card, displays the notification content, and then contracts back into the pill before disappearing into the top bezel.

---

## 🎬 See Curl in Action

<p align="center">
  <img src="Curl.gif" width="700" alt="Curl Dynamic Island demonstration" />
</p>

> **Curl in action:** The notification island smoothly emerges from the top of the screen, expands into a full notification card, displays the content, and retracts back into the compact pill.

---

## 🏝️ How Curl Looks

Curl is designed around a simple animation sequence:

**Compact Pill → Expand → Display → Contract → Hide**

```text
       ┌─────────────────────┐
       │      CURL           │
       └─────────────────────┘
                 ↓
       ┌──────────────────────────────┐
       │  🔔  Telegram                │
       │      New message received    │
       └──────────────────────────────┘
                 ↓
       ┌─────────────────────┐
       │      CURL           │
       └─────────────────────┘
                 ↓
              Hidden
