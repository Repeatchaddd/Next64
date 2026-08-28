# Next64 C64 Game Creator VER 11.0

VER 11.0 adds a general-purpose persistent inventory system whose visual icons are normal project tiles.

## Highlights

- Dedicated Inventory workspace
- 1-32 persistent slots
- Item IDs, names, tile icons, quantities, and maximum stacks
- Initial inventory contents and selected slot
- Configurable tile-grid display room
- Inventory Visual Logic actions and conditions
- Matching Test Play behavior
- Generated C64 inventory storage and runtime routines
- Inventory state persists across room changes

## Also included

- VER 10.0 integrated tile editor
- Software and VIC-II sprite workflows
- Safe **Duplicate and Convert** option for Software-to-VIC conversion
- Rooms, reusable object instances, named paths, tile collision, and custom tile properties
- Multiple `DO` actions per visual event
- Resizable Test Play preview
- Editable Solitaire, Galaga-style, pathing, and maze-chase examples

## Requirements

- Windows with Python 3.10 or newer
- Pillow for PNG features and improved Test Play rendering
- Kick Assembler for C64 compilation
- VICE or real hardware for final validation

Kick Assembler is not included.

## Testing status

The Python editor passes syntax compilation, inventory source generation was exercised, the included Quick Start PDF was visually checked, and the release ZIP passed archive-integrity testing. Generated C64 projects should still be compiled and tested locally with Kick Assembler and VICE.

## Known limitations

Next64 remains an early, actively developed tool. Busy software-sprite scenes may exceed C64 CPU limits, VIC-II multiplexing depends on raster timing and sprite spacing, and some genres still need additional general-purpose logic capabilities.
