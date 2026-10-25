# New Super Mario Bros. DS: Vanilla+ — Native Windows Builder

[Download the current GUI Offline Builder](https://github.com/xcoffeetommyx/NSMB-DS-VanillaPlus-Releases/releases/tag/native-v1.3)

Build a native Windows game from your own clean USA ROM. The builder includes
its dependencies and runs offline. No Python, Git, Visual Studio, or SDK setup
is required. Game code is generated and compiled locally from your ROM.

1. Download **NSMB-VanillaPlus-Offline-Builder.zip** under the release's Assets.
   GitHub's automatic **Source code** archives are not the builder.
2. Extract the entire ZIP to a writable local folder.
3. Open **VanillaPlus Builder.exe**, then choose or drop in your ROM.
4. Select **Build**. The window shows progress, elapsed time, and any
   error code/reason. Compilation happens once; no terminal is needed.
5. Select Play when it finishes. Next time, open **Play-VanillaPlus.exe**.
   Keep it beside the **Support** folder.

The initial download opens to the builder, README.txt, and Support. Required
source, tools, checks, and license notices are kept in Support. Build logs are
available from the GUI. Your supplied ROM is never changed.

## Requirements and play

- Windows 10/11, 64-bit x64 PC, working graphics drivers, and several GB free.
- Clean, untrimmed USA A2DE ROM: **33,554,432 bytes**.
  SHA-256: `9f67fef1b4c73e966767f6153431ada3751dc1b0da2c70f386c14a5e3017f354`.
- Native single-screen widescreen presentation, separate 2D/3D scaling, and
  local campaign co-op with two controllers in one instance.
- Escape opens settings/controller assignments. Alt+Enter toggles exclusive
  fullscreen. Select toggles map information and uses reserve items in stages.

Both ARM9 and ARM7 use static-only execution. The release notes and bundled
Support/docs/VALIDATION.md state the measured build time and exact test scope.
Microphone support remains paused. Retail Mario vs. Luigi and minigame
VS/DS Download Play are unavailable; fixed-layout 2D minigames remain 4:3.
The current builder also fixes the co-op missed-flagpole crash and missing
World 2 jump/coin effects, and avoids re-uploading an unchanged HUD texture.
Native v1.3 also fixes Mario’s offscreen intro movement, flower flicker, the
lightning ground seam, and the shared view/return prompt when one co-op player
dies. Both players dying still uses the normal level exit.
Other documented gameplay limitations remain unchanged.

Share the original builder ZIP, not your built game folder. The local output
contains code and data derived from your ROM; no playable ROM or generated
game executable is included in the download.

## Older releases

The [original v1.0 ROM patch](https://github.com/xcoffeetommyx/NSMB-DS-VanillaPlus-Releases/releases/tag/v1.0)
and earlier native builders remain available for history. Their original tags
and assets are preserved. The guide below applies only to the older ROM patch,
including its separate local-wireless setup.

<details>
<summary>Original v1.0 ROM-patch guide (legacy; preserved)</summary>

NEW SUPER MARIO BROS. DS: VANILLA+
Version 1.0 | USA A2DE | 2026-10-09

A feature-complete Vanilla+ release with the original eight-world campaign,
solo and local co-op in one cartridge, repeatable Wii-style twirls, partner
carrying, and sharper classic enemy artwork.

PATCHING
========
1. Extract this ZIP.
2. Select your clean, unmodified USA A2DE .nds dump as the source in an xdelta3
   compatible patcher. Extract it first if it is inside a ZIP or 7z archive.
3. Select NSMB-DS-VanillaPlus-v1.0-USA.xdelta as the patch.
4. Choose a NEW output filename, such as NSMB-DS-VanillaPlus-v1.0-USA.nds.
5. Apply the patch, then open the output in melonDS.

Command-line equivalent (xdelta3 must be installed):

xdelta3 -d -s "New Super Mario Bros. (USA, Australia).nds" "NSMB-DS-VanillaPlus-v1.0-USA.xdelta" "NSMB-DS-VanillaPlus-v1.0-USA.nds"

Apply directly to the clean DS game. No intermediate donor patch or Wii disc
is needed to apply this release. Do not apply it over another mod or an older
Vanilla+ build. A source/checksum error means the input does not match; do not
force the patch onto a different revision or region.

Supported input:
  Game code: A2DE
  Size: 33554432 bytes
  CRC32: 0197576A
  SHA256: 9f67fef1b4c73e966767f6153431ada3751dc1b0da2c70f386c14a5e3017f354

Expected patched output:
  Size: 45528200 bytes
  SHA256: 035a5df0aded047260d69d28e89eb6e9c218f31452aa8319d92ea34e67fb2397

PLAY AND CONTROLS
=================
Picker: Up/Down to choose Single Player or 2 Player Local Co-op; A to confirm.

Default layout: A jumps; B or Y runs.
Alternate layout: A or B jumps; Y runs.
R: Tap while airborne to twirl. Release and tap again after the 30-frame
   cooldown (about half a second). Multiple twirls work in the same jump;
   holding R does not repeat. Twirls ease falling speed without adding lift.
X: In co-op, tap near your partner to pick them up, then tap again to throw.
   Either Mario or Luigi can carry. Run, jump and twirl while carrying;
   the passenger can jump free after the initial lift. The passenger
   automatically crouches under low ceilings when there is enough room.
Select: Drop the reserve item in BOTH solo and co-op. The usual item-use
   restrictions still apply. The original touchscreen control also remains.
Start: Original pause menu.

Stage camera panning with L/R is disabled. The original solo Luigi selection
shortcut remains. Title/menu shortcuts retain their original inputs.

LOCAL CO-OP
===========
Both devices/emulator instances must use this same build and select co-op.
Choose Mario on one and Luigi on the other, then use the co-op connection
menus. This is local wireless co-op; the release does not add internet play.
The inherited co-op title-menu widescreen toggle is L+R+X.

Solo and co-op share the save through the project's save adapter. Back up an
existing save before switching ROM builds. Emulator save states belong to a
specific ROM build; start normally when moving to v1.0.

INCLUDED FEATURES
=================
- Original DS campaign and power-ups, with solo/local co-op mode selection.
- Repeatable R twirl with Wii timing, falling-speed behavior and twirl sound.
- X partner pickup/throw, Wii carry motions, running/jumping/twirling while
  carrying, passenger escape and automatic crouching under low ceilings.
- Select reserve-item shortcut in both modes.
- Shared solo/co-op save handling.
- Compatible Newer DS enemy/object textures; sharpened Goomba, Koopa and Boo
  sprites; clarity improvements to 183 textures across 87 enemy/boss/hazard
  models. Original geometry, animation rigs and texture memory are preserved.
- Original Mario/Luigi models and power-up colors.

VALIDATION
==========
v1.0 passed a fresh melonDS picker-to-World-1-1 boot and repeated-airborne-twirl
check. Native solo Select checks cover all five reserve items, their drop
animations, an empty reserve, held/re-pressed input and paused input. Items
were seeded in test RAM; the distributed ROM contains no test setup.
Compiled ARM checks cover twirl, carrying, save handling and Select routing.
Asset-preservation checks pass for both engines. The final Select change leaves
the co-op engine byte-identical to the preceding build. The packaged xdelta was
decoded against the clean USA ROM and matched the tested output byte-for-byte.

Earlier user testing reported working melonDS multiplayer without desyncs;
a fresh two-instance wireless session on the final release has not been run.
Full-campaign regression, nds-bootstrap and real DS/3DS hardware compatibility
are not verified. Feature-complete describes the finished feature set.

SHARING
========
Share this ZIP or its xdelta patch. The archive contains the patch, this README,
credits and checksums. No playable ROM, save, BIOS or donor disc is included.
Keep CREDITS.txt with the release.

</details>
