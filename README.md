# New Super Mario Bros. DS: Vanilla+ — Native Windows Builder

[Download the Offline Builder](https://github.com/xcoffeetommyx/NSMB-DS-VanillaPlus-Releases/releases/latest)

Build the native Windows game from your own clean USA ROM. Everything needed
to build is included and works offline. No Python, Git, Visual Studio, SDK
installation, or dependency downloads are required.

## Build and play

1. Download **NSMB-VanillaPlus-Offline-Builder.zip** from the release's Assets.
   GitHub's automatic **Source code** downloads are not the builder.
2. Extract the entire ZIP to a writable local folder.
3. Open **VanillaPlus Builder.exe**, then browse for or drop in your ROM.
4. Select **Build**. The window shows progress, elapsed time, and error details
   if a build fails. The terminal stays hidden.
5. Select **Play** when the build finishes. Afterward, launch
   **Play-VanillaPlus.exe** directly. Keep the **Support** folder beside it.

Compilation is needed once and its duration depends on your PC. Your supplied
ROM is never changed. Share the builder ZIP, not the locally built game folder.
The download contains no playable ROM or generated game executable.

## Requirements

- Windows 10/11, 64-bit x64, working graphics drivers, and several GB free.
- A clean, untrimmed USA A2DE ROM, **33,554,432 bytes**.
- ROM SHA-256: `9f67fef1b4c73e966767f6153431ada3751dc1b0da2c70f386c14a5e3017f354`.

## Features and controls

- Static-only ARM9 and ARM7 execution, with game code compiled locally.
- Single-screen widescreen gameplay and separate 2D menu / 3D resolution settings.
- Local campaign co-op with two controllers in one game instance.
- **Escape:** graphics, controls, and controller assignment settings.
- **Alt+Enter:** toggle exclusive fullscreen.
- **Select:** use a reserve item in stages or toggle the map information panel.
- **R:** repeatable airborne twirl. **X:** pick up or throw a nearby partner.
- Either character can carry; moving and jumping use holding poses. The carrier
  cannot crouch, and the passenger can jump free or crouch automatically under
  low ceilings. Either player can return after dying while their partner lives.

The current build includes reliable minigame startup after earlier menu activity
and corrected widescreen Copy/Erase selection, confirmation, and result screens.
Mega Mushroom pickups and expanded intro geometry are also supported.

## Compatibility notes

Microphone support is paused. Retail Mario vs. Luigi and minigame VS / DS
Download Play are unavailable; fixed-layout 2D minigames retain their original
board dimensions. The bundled **Support/docs/VALIDATION.md** records actual
test coverage and known limitations. These checks are not a claim that every
level, minigame, controller, or PC configuration has been exhaustively tested.

Credits and required source/license notices are included in **Support**.
