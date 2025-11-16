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
