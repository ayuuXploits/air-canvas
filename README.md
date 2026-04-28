# ✋ Air Canvas — Gesture Drawing Studio

> Draw in the air using just your hands. No touch, no mouse — pure computer vision.
---

## 📸 Overview

**Air Canvas** is a browser-based gesture drawing application that uses your webcam and Google's MediaPipe Hands to track your hand movements in real time. Draw, erase, switch colors, and control brush thickness — all without touching a screen.

---

## ✨ Features

| Feature | Description |
|---|---|
| ✏️ Gesture Drawing | Point your right index finger to draw on the canvas |
| 🎨 Color Control | Use your left hand finger count to switch between 5 colors |
| 🖐️ Eraser Mode | Spread all 5 fingers on the right hand to erase locally |
| 📏 Brush Thickness | Pinch left hand to adjust stroke width in real time |
| ↩️ Undo | Ctrl+Z or panel button — up to 20 levels of history |
| ✊ Clear | Make a fist with your left hand to clear the canvas |
| 💾 Export PNG | Save your artwork as a timestamped PNG file |
| ⟺ Mirror Toggle | Flip drawing layer independently of the video feed |
| 📡 Hand Skeleton | Live landmark skeleton drawn on both hands |
| ⚡ FPS Counter | Live rolling average performance indicator |
| 🎬 Onboarding | First-launch guide overlay with gesture instructions |
| 🔲 Collapsible Panel | Full-screen drawing mode with panel hide/show |

---

## 🤌 Gesture Reference

### Right Hand — Drawing

| Gesture | Action |
|---|---|
| ☝️ Index finger only | Draw stroke |
| 🖐️ All 5 fingers spread | Eraser mode |
| ✌️ 2–4 fingers up | Lift pen (pause drawing) |

### Left Hand — Controls

| Gesture | Action |
|---|---|
| 1 finger | Color → Pink |
| 2 fingers | Color → Cyan |
| 3 fingers | Color → Mint |
| 4 fingers | Color → Gold |
| 5 fingers | Color → Flame |
| 🤏 Pinch | Adjust brush thickness |
| ✊ Fist (hold 0.6s) | Clear entire canvas |

---

## 🚀 Quick Start

### Option 1 — Open directly in browser

Just double-click `air_canvas_final.html` or drag it into any Chromium-based browser.

> ⚠️ **Requires a webcam and camera permission.** Works best in Chrome or Edge.

---

### Option 2 — Clone from GitHub

```bash
# Clone the repository
git clone https://github.com/ayuuXploits/air-canvas.git

# Navigate into the project
cd air-canvas

# Open in your default browser (Linux)
xdg-open air_canvas.html

# Open in your default browser (macOS)
open air_canvas.html

# Open in your default browser (Windows)
start air_canvas.html
```

---

### Option 3 — Serve locally with Python (recommended for best performance)

```bash
# Python 3
python3 -m http.server 8080

# Python 2 (legacy)
python -m SimpleHTTPServer 8080
```

Then open your browser at:

```
http://localhost:8080/air_canvas.html
```

---

### Option 4 — Serve with Node.js (`http-server`)

```bash
# Install http-server globally
npm install -g http-server

# Start the server
http-server . -p 8080 --cors

# Open in browser
http://localhost:8080
```

---

### Option 5 — Serve with Live Server (VS Code)

```bash
# Install the Live Server extension in VS Code
# Then right-click air_canvas.html → Open with Live Server
# Or use the terminal:
npx live-server --port=8080
```

---

## 📥 Download via curl

```bash
# Download the app file directly
curl -L https://raw.githubusercontent.com/ayuuXploits/air-canvas/main/air_canvas.html \
     -o air_canvas.html

# Download the README
curl -L https://raw.githubusercontent.com/ayuuXploits/air-canvas/main/README.md \
     -o README.md

# Download both in one go
curl -L https://raw.githubusercontent.com/ayuuXploits/air-canvas/main/air_canvas.html -o air_canvas.html && \
curl -L https://raw.githubusercontent.com/ayuuXploits/air-canvas/main/README.md -o README.md
```

---

## 📤 Push to GitHub

```bash
# Initialize a new repo (if not already)
git init
git remote add origin https://github.com/ayuuXploits/air-canvas.git

# Stage all files
git add .

# Commit
git commit -m "feat: initial release of Air Canvas gesture drawing studio"

# Push to main branch
git push -u origin main
```

If you're updating an existing repo:

```bash
git add air_canvas.html README.md
git commit -m "fix: correct left/right hand detection with mirror mode"
git push
```

---

## 🌐 Deploy to GitHub Pages

```bash
# Make sure your repo is public on GitHub, then:
# Go to Settings → Pages → Source → Deploy from branch → main → / (root)

# Or use the GitHub CLI
gh repo create ayuuXploits/air-canvas --public --source=. --remote=origin --push

# Enable Pages via CLI
gh api repos/ayuuXploits/air-canvas/pages \
  --method POST \
  --field source='{"branch":"main","path":"/"}'
```

Your app will be live at:
```
https://ayuuXploits.github.io/air-canvas/air_canvas.html
```

---

## 🧱 Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 Canvas | Drawing layer and video compositing |
| CSS3 | UI, animations, collapsible panel |
| Vanilla JavaScript | App logic, gesture processing, undo stack |
| [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) | Real-time 21-point hand landmark detection |
| MediaPipe Camera Utils | Webcam frame capture pipeline |
| Google Fonts — Syne + Space Mono | Typography |

No build tools. No frameworks. No dependencies to install. One `.html` file.

---

## 📁 Project Structure

```
air-canvas/
│
├── air_canvas.html           # Main application (single file)
└── README.md                 # This file
```

---

## 🔧 Troubleshooting

**Camera not working?**
- Make sure you have allowed camera permissions in your browser
- Try opening in Chrome or Edge (Firefox has limited MediaPipe support)
- If on `file://`, switch to `localhost` using any server method above

**Hands not detected?**
- Ensure good lighting — avoid strong backlight
- Keep hands within the camera frame
- Stay 40–80 cm from the camera for best accuracy

**Laggy drawing?**
- Close other browser tabs to free up CPU
- Lower your browser zoom to 100%
- Check FPS indicator in the top-right corner — below 15 FPS will cause gaps

**Left/right hand reversed?**
- Click the `⟺ MIRROR` toggle in the top bar — this corrects hand labelling

---

## 📄 License

```
Copyright (c) 2026 ayuuXploits



## 🙌 Author

**ayuuXploits**
- GitHub: [@ayuuXploits](https://github.com/ayuuXploits)

---

> 
