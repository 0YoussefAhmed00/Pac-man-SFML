# Maze Game (SFML, C++20)

A simple grid-based maze game built with SFML. Choose a normal or randomly generated maze, navigate the player, and collect the treasure before time runs out. Includes a clean UI, fullscreen rendering, basic collision, and win/lose screens with sound.

## Features
- Fullscreen 1920×1080 rendering with UI overlay
- Menu with:
  - Normal Maze
  - Generic (Random) Maze
  - Exit
- Smooth grid movement with collision against walls
- Timer HUD (default: 10 minutes)
- Win screen with sound; lose screen when time expires
- Mouse and keyboard support for the menu

## Controls
- Menu:
  - 1: Normal Maze
  - 2: Generic (Random) Maze
  - 3: Exit
  - Mouse: Hover to highlight; click to select
- In-game:
  - Movement: Arrow keys or WASD (handled by `Player`)
  - ESC: Return to menu
- Win/Lose screens:
  - ESC / ENTER / SPACE or click: Return to menu

## Requirements
- Windows 10/11
- Visual Studio 2022 (C++20)
- SFML 2.6.x (graphics, window, system, audio)
- vcpkg (recommended) for dependency management

## Getting Started

1) Clone

2) Install SFML via vcpkg (recommended)
   
3) Open in Visual Studio
- Open the solution or project.
- Set platform to x64 via __Build > Configuration Manager__.
- Ensure C++ standard is C++20 via __Project > Properties > C/C++ > Language > C++ Language Standard__.
- Set working directory so assets load correctly:
  - __Project > Properties > Debugging > Working Directory__: `$(ProjectDir)` or the repository root.

4) Run
- Start without debugging (Ctrl+F5).

Note the casing difference between `assets` and `Assets` as used by the code. On case-sensitive filesystems, keep folder names exactly as shown.

## Configuration Tips
- Time limit:
  - `Game` class has `float timeLimitSec = 600.f;` (10 minutes). Adjust as needed.
- Window mode and size:
  - In `Game::Game()`, change `VideoMode(1920, 1080), "Maze Game", Style::Fullscreen` to your preferred resolution or use `Style::Default` for windowed mode.
- Camera zoom:
  - Adjust `zoomFactor` in the `Game` class (default `1.10f`).
- Asset paths:
  - Fonts: `assets/fonts/...`
  - Win sound: `Assets/Audio/winsound.mp3`
  - Keep paths and casing consistent with your filesystem.

## Troubleshooting
- Black screen or missing text/sound:
  - Check __Project > Properties > Debugging > Working Directory__ points to the repo or project folder containing `assets` and `Assets`.
- Missing SFML DLLs at runtime:
  - Ensure you built x64 and installed `sfml:x64-windows`. With vcpkg integration, VS will resolve the paths automatically.
- No audio:
  - Verify `Assets/Audio/winsound.mp3` exists and your output device is available.
- Case-sensitive paths:
  - Ensure the `assets` vs `Assets` folder names match exactly.

## Links
- itch.io page: https://youssef-ahmed-m.itch.io/simple-pac-man
- Repository: https://github.com/0YoussefAhmed00/Pac-man-SFML

## Acknowledgments
- SFML: https://www.sfml-dev.org/
- Fonts:
  - `Fascinate-Regular.ttf`
  - `WDXLLubrifontTC-Regular.ttf`
  Ensure you have the right to redistribute any third-party assets you include.
