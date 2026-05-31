<div align="center">
     
# ✋ Air Canvas — Gesture Drawing Studio

[![MediaPipe](https://img.shields.io/badge/MediaPipe-Hands-00C853?style=for-the-badge&logo=google&logoColor=white)](https://developers.google.com/mediapipe)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-red.svg?style=for-the-badge)](#-license)
[![Platform](https://img.shields.io/badge/Platform-Chrome%20%7C%20Edge%20%7C%20Brave-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.google.com/chrome/)
[![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=for-the-badge)](https://github.com/ayuuXploits/air-canvas)

[**🚀 Live Demo**](https://ayuuXploits.github.io/air-canvas/) &nbsp;·&nbsp; [**🐛 Report Bug**](https://github.com/ayuuXploits/air-canvas/issues/new?assignees=&labels=bug&template=bug_report.md&title=%5BBug%5D+) [**✨ Request Feature**](https://github.com/ayuuXploits/air-canvas/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=%5BFeature%5D+)


> Draw in the air using just your hands. No touch, no mouse — pure computer vision.

![Main Header](./docs/air_canvas2.png)
![Main Header](./docs/aircanvas1.png)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Gesture Reference](#-gesture-reference)
- [Shape Mode](#-shape-mode)
- [Move Mode](#-move-mode)
- [Quick Start](#-quick-start)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 📸 Overview

**Air Canvas** is a browser-based gesture drawing application that uses your webcam and Google's MediaPipe Hands to track your hand movements in real time. Draw freehand strokes, drop precise shapes, move objects around the canvas, and control colors and brush thickness — all without touching a screen.

One `.html` file. No install. No frameworks. Just open and draw.

---

## ✨ Features

| Feature | Description |
|---|---|
| ✏️ Freehand Drawing | Point your right index finger to draw smooth quadratic-curve strokes |
| 🔲 Shape Mode | Draw precise lines, rectangles, and ellipses with a two-gesture commit flow |
| ✋ Move Mode | Grab any stroke or shape with a closed fist and drag it anywhere on the canvas |
| 🎨 Color Control | Use your left hand finger count to switch between 5 colors with a flash overlay |
| 🗑️ Eraser Mode | Spread all 5 fingers on the right hand or enable via panel to erase objects |
| 📏 Brush Thickness | Pinch left hand to adjust stroke width in real time with smooth interpolation |
| ↩️ Undo | Ctrl+Z or panel button — up to 30 levels of deep-copy object history |
| ✊ Clear | Make a fist with your left hand and hold for 0.6 s to clear the canvas |
| 💾 Export PNG | Save your artwork as a timestamped PNG file |
| ⟺ Mirror Toggle | Flip the drawing layer independently of the video feed |
| 📡 Hand Skeleton | Live 21-point landmark skeleton drawn on both hands |
| ⚡ FPS Counter | Live rolling-average performance indicator |
| 🎬 Onboarding | First-launch guide overlay with full gesture reference |
| 🔲 Collapsible Panel | Full-screen drawing mode with animated slide-in/out side panel |
| 🟡 Grab Progress Arc | Animated arc ring shows fist-hold charge progress before an object is grabbed |
| 🖼️ Object Model | Every stroke and shape is stored as a data object — fully movable and undoable |

---

## 🤌 Gesture Reference

### Right Hand — Drawing & Interaction

| Gesture | Action |
|---|---|
| ☝️ Index finger only | Draw stroke (Freehand) / Set shape start point (Shape) |
| ✌️ 2 fingers up | Commit shape (Shape mode) / Lift pen (Freehand) |
| 🖐️ All 5 fingers spread | Eraser mode — erase objects under cursor |
| ✊ Closed fist (hold) | Grab object (Move mode) — watch the gold arc fill to confirm |
| 🖐️ Open hand | Release grabbed object (Move mode) |

### Left Hand — Controls

| Gesture | Action |
|---|---|
| 1 finger | Color → Pink |
| 2 fingers | Color → Cyan |
| 3 fingers | Color → Mint |
| 4 fingers | Color → Gold |
| 5 fingers | Color → Flame |
| 🤏 Pinch | Adjust brush thickness (spread = thicker, narrow = thinner) |
| ✊ Fist (hold 0.6 s) | Clear entire canvas |

---

## 🔲 Shape Mode

Switch to **Shape** mode in the side panel, then choose **Line**, **Rect**, or **Circle**:

