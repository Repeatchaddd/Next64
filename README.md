# Next64 C64 Game Creator

Next64 is a visual game creator for the Commodore 64. It combines sprite, tile, room, object, path, inventory, and visual-logic editors with a Kick Assembler export pipeline.

The project is being developed by **Next64 Studios** for people who want to create new C64 games without writing an entire engine from scratch.

> **Project status:** Early but usable. Next64 can create and test small projects, but it is still under active development and has known limitations. Save backups and test generated games in VICE or on real hardware.

## Current release

**VER 11.0** adds a persistent tile-based inventory system while retaining the integrated tile editor, software sprites, VIC-II sprites, rooms, paths, reusable visual behaviors, and Kick Assembler generation.

[Download the current full build](next64_game_creator_ver_11_0.zip)

The ZIP contains the editor, examples, generated-ASM examples, Windows launcher, README, and current Quick Start PDF.

## Current capabilities

### Graphics

- Software-rendered hires and multicolor sprites
- Optional VIC-II hardware sprites
- Sprite IDs from 0-255 per level
- Multiple animation frames with durations and preview playback
- Per-level Sprite 0 template for mode and shared-color inheritance
- Software-to-VIC conversion warning with a recommended **Duplicate and Convert** option
- C64 palette indices preserved in generated output

### Tiles and rooms

- Integrated C64 tile pixel editor
- Hires and multicolor tiles
- Tile-sheet image import
- Sky Strike tileset import
- Per-tile collision class: None, Solid, or Hazard
- Four custom byte properties (`P0-P3`) per tile
- Tile-map painting and individual room layouts
- Explicit player starts and automatic edge entry between rooms
- Persistent object state between room changes

### Objects and visual logic

- Reusable object definitions and independent room instances
- Multiple `DO` actions in one visual event block
- Keyboard, collision, animation, variable, path, tile, and room events
- Built-in object properties including X, Y, Active, Room, Frame, and `P0-P7`
- Named paths with Loop, Patrol, and Once modes
- Generic grid/maze helpers and queued-direction movement

### Inventory - VER 11.0

- 1-32 persistent inventory slots
- Item IDs, names, tile icons, quantities, and maximum stack sizes
- Initial slot contents and selected slot
- Configurable tile-grid display room
- Add, remove, use, move, select, and render actions
- Contains-item, slot-equals, and minimum-quantity conditions
- Matching Test Play and generated C64 runtime behavior

### Testing and export

- Resizable Test Play window with aspect-preserving C64 preview
- Generated Kick Assembler source and binary resources
- `.prg` build support when `KickAss.jar` is configured
- Standard-memory projects plus optional REU setting
- Editable Solitaire, Galaga-style, pathing, and maze-chase examples

## Requirements

- Windows 10 or Windows 11 for the included launcher
- Python 3.10 or newer
- Tkinter, normally included with Windows Python
- [Pillow](https://pypi.org/project/Pillow/) for PNG import/export and the fastest Test Play drawing path
- [Kick Assembler](https://theweb.dk/KickAssembler/) to compile generated source into a C64 `.prg`
- [VICE](https://vice-emu.sourceforge.io/) or Commodore 64 hardware for final testing

Install Pillow from Command Prompt:

```bat
py -m pip install pillow
```

## Running the editor

1. Download and extract the full ZIP.
2. Keep all included files and folders together.
3. Run `RUN_EDITOR.bat`.
4. If Windows cannot find Python, install Python and enable **Add Python to PATH** during installation.

You can also start it directly:

```bat
py next64_game_creator.py
```

## Building a generated C64 game

1. Open the **Build** tab.
2. Select your `KickAss.jar` file.
3. Generate the ASM folder.
4. Use **Build PRG**, or run the generated `build.bat` inside that folder.
5. Test the resulting `.prg` in VICE before trying real hardware.

`KickAss.jar` is not distributed with Next64.

## Recommended first project workflow

1. Create a level.
2. Create Sprite 0 first; it controls that level's graphics mode and shared colors.
3. Add sprites and animation frames.
4. Create objects that use those sprites.
5. Create or import tiles in **Tiles**.
6. Paint a room and place objects in **Rooms**.
7. Attach editable behavior in **Visual Logic**.
8. Use **Test Play** frequently.
9. Save the `.n64game` project.
10. Generate, compile, and test the C64 build.

## Known limitations

- Next64 is under active development and is not yet a complete replacement for a mature commercial game engine.
- Generated C64 output still needs testing in VICE or on hardware.
- The editor cannot automatically repair room placements after a sprite is converted to a larger VIC-II sprite.
- Large or busy software-sprite scenes may exceed practical C64 CPU limits.
- VIC-II multiplexing depends on sprite spacing and raster timing.
- Tile Local color is currently stored per tile, not separately for every 8x8 character cell within a larger tile.
- The inventory renderer uses normal room tiles; the configured grid must fit inside the room's 40x25 tile-map storage.
- Some game genres will still require additional general-purpose editor actions or custom ASM calls.
- REU-enabled enhancements remain optional and must not be assumed on a standard C64.

Please report reproducible problems through [GitHub Issues](../../issues). Include the Next64 version, renderer and graphics mode, steps to reproduce, generated build error if applicable, and whether the issue occurs in Test Play, VICE, or both.

## Repository layout

The current repository distributes complete versioned ZIP builds. The source, examples, manual, and generated reference projects are inside the ZIP so compatible files stay together.

Future repository organization may expose the source tree directly as the project stabilizes.

## Contributing

Bug reports, carefully scoped feature suggestions, documentation corrections, and reproducible test projects are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

No open-source license has been selected yet. Until a license is added, copyright remains with the project owner and normal copyright restrictions apply.

## Credits

Developed by **Next64 Studios**.

Next64 is an independent project and is not affiliated with Commodore, the current owners of the Commodore trademarks, Kick Assembler, or the VICE project.
