# Roblox Parkour System

This is a modular 2D-style parkour system for Roblox. It includes smooth movement, double jump, wall climbing, dynamic speed adjustment, and custom animations. It’s built with local scripts, raycasting, and TweenService for camera and character effects.

---

## 🎮 Features

* 🕹️ 2D movement system with locked camera
* ⏫ Double jump with animation
* 🧱 Wall climbing with smooth vertical movement and jump-off
* 🏃‍♂️ Speed changes depending on ascending or descending terrain
* 🎥 Running and climbing animations
* 📷 Custom camera control with direction tweening

---

## 📁 Modules and Scripts

### `Camera and Movement`

* Handles directional movement (left/right)
* Controls camera position in 2D space
* Responds to key inputs and adjusts movement direction

### `Double_Jump`

* Detects jump state
* Allows second jump while airborne
* Plays custom animation on double jump

### `Increasing Speed`

* Uses raycasting to detect terrain angles
* Tweens camera FOV and adjusts walk speed based on slope direction

### `Running Animation`

* Plays/pauses running animation depending on movement state

### `WallClimbing System`

* Detects walls using raycasts
* Enables vertical climbing with animation
* Stops climbing on spacebar press or when touching ground

---

## 🔧 Requirements

* `rbxassetid` animations for running, climbing, and double jump
* Animator object inside the character’s Humanoid
* Optional: Tag Editor for wall tagging (`Wall` tag used)

---

## 🧪 Example Usage

```lua
-- Load and use the parkour handler module
local Parkour = require(path.to.ParkourHandler)

-- Move the player left/right and jump is automatic via input
-- To trigger wall climbing when needed:
Parkour:TryWallClimb(player.Character)

-- To perform a double jump:
Parkour:EnableDoubleJump()
```

---

## 📌 Notes

* Uses `RenderStepped` for smooth updates
* All movement is local; ideal for single-player or replicated manually for multiplayer
* System assumes a 2D layout but can be modified for 3D

---

## 📞 Contact

Made by [DevChpL](https://github.com/DevChpL)
Feel free to use this system or reach out for help integrating it into a larger project.
