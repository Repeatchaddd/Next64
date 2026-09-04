# Next64 C64 Game Creator

Next64 is a visual game creator for the Commodore 64. It combines sprite, tile, scrolling-room, object, path, inventory, save-game, UI/HUD, audio/music, validation, and visual-logic editors with a Kick Assembler export pipeline.

The project is developed by **Next64 Studios** for people who want to create new C64 games without writing an entire engine from scratch.

> **Project status:** Early but usable. Next64 can create and test small projects, but it is still under active development and has known limitations. Keep backups and test generated games in VICE or on real hardware.

## Current release

**VER 17.0** adds integrated SID sound-effect design and a three-voice music pattern editor, with editor previews, project persistence, generated C64 playback routines, and Visual Logic control.

[Download the current full build](next64_game_creator_ver_17_0.zip)

The ZIP contains the editor, branded splash artwork, examples, generated-ASM examples, Windows launcher, README, and the current Quick Start PDF.

## Current capabilities

### Editor experience

- Branded Next64 Studios startup splash
- Dark navy editor theme with blue, cyan, lavender, and warning accents
- Coordinated tabs, panels, buttons, fields, menus, lists, tables, logs, and status bar
- Authentic C64/project colors preserved inside graphics and Test Play canvases

### Graphics

- Software-rendered hires and multicolor sprites
- Optional VIC-II hardware sprites
- Sprite IDs from 0-255 per level
- Multiple animation frames with durations and preview playback
- Per-level Sprite 0 template for mode and shared-color inheritance
- Safe **Duplicate and Convert** Software-to-VIC workflow
- C64 palette indices preserved in generated output

### Tiles, rooms, and cameras

- Integrated hires and multicolor C64 tile editor
- Tile-sheet image and Sky Strike tileset import
- Per-tile None, Solid, or Hazard collision class
- Four custom byte properties (`P0-P3`) per tile
- Room tile-map painting and reusable object placement
- Rooms from 320x200 through 512x256 in 8-pixel steps
- Fixed or object-following cameras with tile-aligned scrolling
- World-coordinate game logic with camera-relative rendering
- Explicit player starts, automatic edge entry, and persistent room state

### Objects and visual logic

- Reusable object definitions and independent room instances
- Multiple `DO` actions in one visual event block
- Keyboard, collision, animation, variable, path, tile, room, inventory, and save events
- Built-in object properties including X, Y, Active, Room, Frame, and `P0-P7`
- Named paths with Loop, Patrol, and Once modes
- Generic grid/maze helpers and queued-direction movement

### Inventory, save games, and UI/HUD

- 1-32 persistent inventory slots with item definitions, quantities, and tile icons
- Configurable inventory tile-grid rendering
- Versioned C64 disk saves using KERNAL SAVE/LOAD routines
- Selectable variable, inventory, and live-object save data
- Reusable HUD layouts assignable to multiple levels
- Tile, variable-number, and variable-bar HUD elements
- Matching editor Test Play and generated-runtime behavior

### Audio and music

- SID sound-effect editor with waveform, frequency, ADSR, pulse width, and duration controls
- Three-voice note/rest pattern editor with tempo and looping
- Editor previews for sound effects and Voice 1 melodies
- Visual Logic actions to play sounds, start music, and stop music
- Generated `generated_audio.asm` SID playback runtime

### Validation, testing, and export

- Full-project Validator for missing references, bounds, incompatible settings, and common control-property mistakes
- Test Play debug overlays for objects, collisions, IDs, properties, tiles, and held keys
- Pause and single-frame stepping
- Resizable Test Play window with aspect-preserving C64 preview
- Generated Kick Assembler source and binary resources
- `.prg` build support when `KickAss.jar` is configured
- Standard-memory projects plus an optional REU setting
- Editable Solitaire, Galaga-style, pathing, and maze-chase examples

## Requirements

- Windows 10 or Windows 11 for the included launcher
- Python 3.10 or newer
- Tkinter, normally included with Windows Python
- [Pillow](https://pypi.org/project/Pillow/) for PNG support, splash artwork, and the fastest Test Play drawing path
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

## Recommended workflow

1. Create a level.
2. Create Sprite 0 first; it controls that level's graphics mode and shared colors.
3. Add sprites and animation frames.
4. Create objects that use those sprites.
5. Create or import tiles in **Tiles**.
6. Configure and paint rooms, including camera settings, in **Rooms**.
7. Create sound effects or music in **Audio / Music**, then attach editable behavior in **Visual Logic**.
8. Use **Test Play** frequently.
9. Run **Full Validation** and resolve errors.
10. Save the `.n64game` project, generate, compile, and test the C64 build.

## Known limitations

- Next64 is under active development and is not yet a complete replacement for a mature commercial game engine.
- Generated C64 output still needs testing in VICE or on hardware.
- Large or busy software-sprite scenes may exceed practical C64 CPU limits.
- VIC-II multiplexing depends on sprite spacing and raster timing.
- Scrolling rooms currently require 8x8 tiles and are limited to 512x256 pixels.
- Tile Local color is stored per tile, not separately for every 8x8 character cell within a larger tile.
- HUDs are tile-based; static text must currently be drawn as tiles.
- Music currently uses note/rest rows with one shared frames-per-row tempo; filters, slides, vibrato, instrument changes, and SID-song import remain future expansions.
- Some game genres will still require additional general-purpose editor actions or custom ASM calls.
- REU-enabled enhancements remain optional and must not be assumed on a standard C64.

Please report reproducible problems through [GitHub Issues](../../issues). Include the Next64 version, renderer and graphics mode, steps to reproduce, generated build error if applicable, and whether the issue occurs in Test Play, VICE, or both.

## Repository layout

The repository distributes complete versioned ZIP builds. Source, examples, manual, and generated reference projects stay together inside each ZIP.

## Contributing

Bug reports, carefully scoped feature suggestions, documentation corrections, and reproducible test projects are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

No open-source license has been selected yet. Until a license is added, copyright remains with the project owner and normal copyright restrictions apply.

## Credits

Developed by **Next64 Studios**.

Next64 is an independent project and is not affiliated with Commodore, the current owners of the Commodore trademarks, Kick Assembler, or the VICE project.
