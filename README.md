# 🏃 Pixel Runner — Android Game

A fun arcade runner/platformer for Android built with **Kotlin + Canvas (SurfaceView)**.

---

## Features
| Feature | Details |
|---|---|
| **5 Levels** | Forest → Desert → Ice Cave → Lava Fields → Sky Fortress |
| **Double Jump** | Tap twice to double-jump over tall obstacles |
| **Floating Platforms** | Land on them to avoid ground-level obstacles |
| **Coin Collection** | 🪙 Collect coins for bonus score points |
| **Particles** | Coin sparkle + death explosion effects |
| **Progress Bar** | HUD shows score progress toward level goal |
| **Level Unlock** | Levels unlock sequentially on completion |
| **Pause** | Tap top-left corner to pause/resume |
| **60 FPS Loop** | Smooth SurfaceView game loop |

---

## Project Structure
```
app/src/main/java/com/example/runnergame/
├── game/
│   ├── GameConstants.kt   — Tunable game parameters & level configs
│   ├── GameEngine.kt      — Core physics, spawning, collision logic
│   ├── GameRenderer.kt    — Canvas drawing (background, player, UI)
│   └── GameView.kt        — SurfaceView + game loop thread
├── model/
│   └── GameObjects.kt     — Player, Obstacle, Coin, Platform data classes
└── ui/
    ├── MainActivity.kt        — Home screen
    ├── LevelSelectActivity.kt — Level picker (with lock/unlock)
    ├── GameActivity.kt        — Hosts GameView
    └── GameOverActivity.kt    — Score summary + retry/menu
```

---

## How to Open in Android Studio

1. **Open Android Studio** (Hedgehog / Iguana or later recommended)
2. Choose **"Open"** and select the `RunnerGame` folder
3. Wait for Gradle sync to complete
4. Connect an Android device or start an emulator (API 21+, landscape orientation)
5. Press **▶ Run**

---

## Controls (Touch)
| Gesture | Action |
|---|---|
| Tap (anywhere right of edge) | Jump (tap again mid-air for double jump) |
| Tap top-left corner (~15% of screen width) | Pause / Resume |

---

## Tuning the Game
All game parameters are in `GameConstants.kt`:
- **Speed**, **obstacle intervals**, **coin intervals**, **target scores** per level
- **Gravity** and **jump velocity**
- **VIRTUAL_WIDTH / VIRTUAL_HEIGHT** — the game's internal resolution (scales to any screen)

---

## Requirements
- Android Studio Hedgehog (2023.1.1) or newer
- Android SDK 34
- Kotlin 1.9
- Min SDK: API 21 (Android 5.0)
