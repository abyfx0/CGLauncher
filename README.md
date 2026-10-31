
# CG Launcher

A lightweight, native macOS app/game launcher built with SwiftUI and AppKit. Inspired by the clean grid aesthetic of the Astris frontend, **CG Launcher** organizes your native Mac apps/games in a customizable, borderless grid with real-time 3D hover parallax, native Liquid Glass overlays, and automatic background playtime tracking.

![macOS](https://img.shields.io/badge/macOS-14.0%2B%20%7C%2026.0%2B-000000?style=flat&logo=apple&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-5.9%2B-F05138?style=flat&logo=swift&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-Apple%20Silicon%20%26%20Intel-blue?style=flat)

---

## Screenshots

| Library Grid | 3D Hover & Liquid Glass |
| :---: | :---: |
| <img width="771" height="659" alt="App_screen1" src="https://github.com/user-attachments/assets/8c1f3a5a-551b-4bdc-afad-8e7c0365e6a5" /> | https://github.com/user-attachments/assets/5dcd2b2c-a2db-478a-bb60-2ae77154c1a8 |

---

## Features

- **Native macOS Performance:** Built from the ground up with SwiftUI and `NSWorkspace` for near-zero idle CPU and memory overhead.
- **Automatic Playtime Tracking:** Monitors launched game processes by PID (`NSRunningApplication`) and records exact session durations the moment the game terminates.
- **Interactive 3D Parallax & Liquid Glass:** Smooth 60/120fps pointer-tracking 3D tilt animations paired with macOS's native `.glassEffect` play button overlay.
- **Zero-Config Icon Extraction:** Automatically extracts and caches 512×512 retina app icons directly from macOS `.app` bundles.
- **Dynamic Grid Scaling:** Floating bottom-right slider resizes game covers on the fly while preserving text legibility and layout proportions.
- **Persistent State:** Automatically saves your game library, cumulative playtime, icon sizing preferences, and exact window coordinates across restarts.

---

## Installation

### Direct Download
1. Download the latest `CG-Launcher-v1.0.0.dmg` from the [Releases](https://github.com/abyfx0/CGLauncher/releases) page.
2. Open the `.dmg` file and drag **CG Launcher.app** into your **Applications** folder.
3. **First Launch (Gatekeeper Bypass):** Because this app is distributed outside the Mac App Store without a paid Apple Developer ID, macOS will flag it as an unsigned binary on first run. To open it:
   - **Finder Method:** Right-click (or `Control`-click) **CG Launcher.app** in your `/Applications` folder and select **Open**.
   - **Terminal Method:** Run the following command to clear the quarantine attribute:
     ```bash
     xattr -cr "/Applications/CG Launcher.app"
     ```
---

## Usage

- **Add a Game:** Click the + button in the top-right toolbar and select any macOS .app bundle.
- **Launch a Game:** Double-click any game cover in the grid. Playtime is automatically calculated and saved when you quit the game.
- **Resize Covers:** Drag the floating slider in the bottom-right corner to scale the grid dynamically.
- **Remove a Game:** Right-click a game cover and select Remove from Library (this only removes the entry from CG Launcher; your .app bundle remains untouched on disk).

---

## License

**Distributed under the MIT License. See LICENSE for more information.**
