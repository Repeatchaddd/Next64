# Next64 C64 Game Creator VER 16.0

VER 16.0 gives the complete editor a cohesive Next64 Studios appearance while retaining all game-creation features and project compatibility from earlier versions.

## Highlights

- Dark navy Next64 Studio editor theme
- Layered blue panels with cyan focus and selection accents
- Lavender pressed states and restrained red/amber warning accents
- Compact branded command header
- Prominent Build PRG action
- Coordinated tabs, controls, menus, lists, tables, logs, scrollbars, and status bar
- Authentic C64/project colors preserved in graphics canvases and Test Play
- Bundled branded startup splash
- Updated six-page Quick Start manual

## Major systems included

- Cameras and tile-aligned scrolling rooms up to 512x256
- Reusable level-assigned UI/HUD layouts
- Versioned C64 disk save games
- Full-project Validator and Test Play debug overlays
- Persistent tile-based inventory
- Integrated tile and sprite editors
- Software sprites and optional VIC-II hardware sprites
- Reusable object instances, Visual Logic, paths, and editable examples

## Compatibility

- Existing 320x200 projects remain fixed-camera rooms.
- Existing `.n64game` projects remain supported.
- Editor theming does not alter generated VIC-II color indices or project artwork.
- Standard-memory projects continue to work without requiring an REU.

## Requirements

- Windows with Python 3.10 or newer
- Tkinter, normally included with Windows Python
- Pillow for PNG support, splash artwork, and improved Test Play rendering
- Kick Assembler for C64 compilation
- VICE or real hardware for final validation

Kick Assembler is not included.

## Testing status

- Python source passed syntax compilation.
- The full release ZIP passed archive-integrity and required-file checks.
- The Quick Start PDF was rendered and visually checked across all six pages.
- Generated games should still be compiled and tested locally with Kick Assembler and VICE.

## Known limitations

Next64 remains an early, actively developed tool. Scrolling rooms currently require 8x8 tiles and are limited to 512x256. Busy software-sprite scenes may exceed C64 CPU limits, VIC-II multiplexing depends on raster timing and sprite spacing, and some genres still require additional general-purpose logic capabilities or custom ASM calls.
