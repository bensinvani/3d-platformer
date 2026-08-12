# Platformer 3D

A 3D endless-runner prototype built in Unity 6 (URP). The player auto-runs forward,
steers left/right to weave through obstacles, and scores a point for each obstacle
cleared. Colliding with an obstacle restarts the run.

## Tech

- **Unity** 6000.0.40f1
- **Render pipeline** Universal RP 17.0.4
- **Packages** Cinemachine 3.1.5, Input System 1.13.0, AI Navigation 2.0.6, TextMesh Pro

## Gameplay

| Element | Behaviour |
|---|---|
| Movement | Constant forward velocity, horizontal steering on the `Horizontal` axis |
| Scoring | `OnTriggerEnter` with an `Obstacle` increments the score, shown via TextMesh Pro |
| Fail state | `OnCollisionEnter` with an `Obstacle` reloads the active scene |

Core logic lives in [`Assets/Scripts/PlayerMovement.cs`](Assets/Scripts/PlayerMovement.cs).

## Running it

1. Clone the repo.
2. Open the folder with Unity Hub using editor version **6000.0.40f1**.
3. Open `Assets/Scenes/GameScene.unity` and press Play.

## AI-assisted editing

This project has [MCP for Unity](https://github.com/CoplayDev/unity-mcp) installed, which
lets an MCP client (Claude Code, Cursor, etc.) read and modify the scene, GameObjects, and
scripts directly in the running editor. See the package under
`Window → MCP for Unity` after the editor imports it.
