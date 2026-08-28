# Changelog

This file tracks public Next64 C64 Game Creator releases. Older internal revisions are summarized where appropriate.

## VER 11.0 - Persistent tile-based inventory

- Added a dedicated Inventory workspace.
- Added 1-32 persistent slots with item ID and quantity storage.
- Added item definitions with name, tile icon, and maximum stack size.
- Added configurable initial contents and selected slot.
- Added configurable inventory room, grid position, columns, and empty-slot tile.
- Added inventory Visual Logic conditions and actions.
- Added matching Test Play behavior.
- Added generated C64 inventory arrays and runtime routines.
- Retained all VER 10.0 tile-editor and VER 09.12 runtime improvements.

## VER 10.0 - Integrated tile editor

- Integrated the hardware-constrained tile workspace derived from Sky Strike Level Editor VER 11.2.
- Added a dedicated Tiles tab.
- Added hires and multicolor tile painting and erasing.
- Added tile creation, duplication, deletion, clearing, and PNG load/save.
- Connected edited tiles to rooms, Test Play, project saving, collision data, properties, and ASM export.
- Added a warning before destructive Software-to-VIC conversion.
- Added **Duplicate and Convert** to preserve the original software sprite.

## VER 09.12 - Input and rendering reliability

- Improved C64 W/A/S/D/SPACE input reliability.
- Added queued-direction grid movement tools.
- Corrected software-hires foreground color behavior.
- Improved atomic VIC-II sprite register updates.
- Retained tile-render, dirty-rectangle, freeze, and Test Play performance fixes.

## Earlier development

Earlier revisions established:

- Software and VIC-II sprite editing
- Animation frames and preview
- Objects and reusable room instances
- Visual Logic and multiple actions per event
- Rooms, tilemaps, collision, and custom tile properties
- Named paths
- Kick Assembler generation and `.prg` build support
- Editable example projects
