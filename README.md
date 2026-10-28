# Floating To-Do

Native floating task list for macOS and Windows. Current source version: **1.3.3**.

## Downloads and source

- `FloatingToDo-Mac-Latest.zip`: universal Intel + Apple Silicon app, macOS **12.6 or newer**. Ad-hoc signed, not notarized. macOS 12.6 physical hardware has not been tested.
- `FloatingToDo-Source.zip`: Mac SwiftUI/AppKit project.
- `FloatingToDo-Windows-Source.zip`: Windows Tauri/Rust/JavaScript project. Extract before building.
- Windows installer: Actions → latest successful **Build Windows trial** run → artifact **FloatingToDo-Windows-x64**. The installer targets Windows 10/11 x64 and is unsigned.

## Current behavior

Right-click the circular widget for Quit and Quick Add. Quick Add supports deadlines. Click outside the panel to collapse it; the panel X asks before quitting. Gear settings include task size, text alignment, English/Chinese, and 12/24-hour time. Marquee-select To-Do tasks to reorder the group or drag it to trash to move it into Cancelled; marquee-select completed/cancelled tasks from blank list space, then drag the selected group onto the footer trash and confirm deletion.

English text uses a larger regular Courier New face. Chinese uses PingFang Light on macOS and the installed Windows Chinese fallback on Windows; no Apple fonts are redistributed.

Tasks stay local. This repository contains no user task data. On newer macOS versions, clicking wallpaper may separately trigger the user's system-level Show Desktop setting; the app does not alter that preference.

## Build

Mac: extract the Mac source, run `./build.sh` on a Mac with Apple Command Line Tools.
Windows: extract the Windows source and run `pnpm install --frozen-lockfile`, `pnpm test`, and `pnpm build:windows` on Windows with Rust and the Windows desktop build tools. The repository workflow extracts the Windows source ZIP automatically.
