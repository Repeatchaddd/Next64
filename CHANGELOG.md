# Changelog

This file tracks public Next64 C64 Game Creator releases. Older internal revisions are summarized where appropriate.

## VER 17.0 - Audio and music editor expansion

- Added a SID sound-effect editor with waveform, frequency, ADSR, pulse-width, and duration controls.
- Added a compact three-voice music pattern editor with note/rest rows, tempo, and looping.
- Added editor previews for effects and Voice 1 melodies.
- Added Play Sound, Play Music, and Stop Music Visual Logic actions.
- Added project save/load support for audio resources.
- Added generated C64 SID playback through `generated_audio.asm`.
- Preserved compatibility with earlier `.n64game` projects.

## VER 16.0 - Next64 Studio editor theme

- Redesigned the complete editor to match the branded startup artwork.
- Added dark navy workspaces, layered blue panels, cyan focus/selection states, lavender pressed states, and restrained warning accents.
- Added a compact Next64 Studios command header and prominent Build PRG action.
- Restyled tabs, controls, menus, lists, tables, logs, scrollbars, and the status bar.
- Preserved project-defined C64 colors in sprite, tile, room, and Test Play canvases.
- Centralized the theme so future ttk controls inherit the same appearance.

## VER 15.1 - Branded startup splash

- Added the bundled Next64 Studios splash artwork.
- Added a centered borderless startup window while the editor initializes.
- Kept the workspace hidden until initialization completes to prevent window flashing.
- Added a lightweight fallback when Pillow or the image is unavailable.

## VER 15.0 - Cameras and scrolling rooms

- Added room sizes from 320x200 through 512x256 in 8-pixel steps.
- Added fixed and object-following camera modes with initial position controls.
- Added full-world room editing with a visible 320x200 viewport outline.
- Kept logic and collision in world coordinates while rendering sprites camera-relative.
- Added clamped, tile-aligned camera movement and full-size exported tilemaps.
- Preserved compatibility with existing fixed-camera 320x200 projects.

## VER 14.1 - Save-game compile correction

- Replaced long 6502 relative branches in generated save header validation with local branches and absolute jumps.
- Prevented `SaveGameBadData` branch-distance failures in larger save payloads.

## VER 14.0 - Reusable UI/HUD layouts

- Added reusable HUD layouts assignable to multiple levels.
- Added fixed tile, variable-number, and variable-bar elements.
- Added matching Test Play and generated C64 HUD rendering.
- Added HUD validation for assignments, bounds, variables, and tilesets.

## VER 13.0 - Save-game support

- Added a Save Game workspace with disk filename, device number, and selectable state groups.
- Added save/load/reset actions and status conditions to Visual Logic.
- Added versioned C64 snapshots using standard KERNAL SAVE/LOAD routines.
- Added matching in-memory Test Play snapshot behavior.

## VER 12.1 - Validator correction

- Corrected direction-property validation so every Set Direction route is checked independently.

## VER 12.0 - Validation and Test Play debugging

- Added full-project validation for missing references, placement errors, settings, and common control-property mistakes.
- Added Test Play overlays for boxes, solid/hazard tiles, IDs, and P0-P7 values.
- Added pause and exact single-frame stepping.

## VER 11.0 - Persistent tile-based inventory

- Added a dedicated Inventory workspace.
- Added 1-32 persistent slots, item definitions, stacking, initial contents, and selected slot.
- Added inventory Visual Logic conditions/actions and matching Test Play/runtime behavior.

## VER 10.0 - Integrated tile editor

- Added a dedicated hardware-constrained Tiles workspace.
- Added hires and multicolor painting, tile management, PNG load/save, collision, properties, Test Play, and ASM export.
- Added safe Software-to-VIC conversion with **Duplicate and Convert**.

## VER 09.12 - Input and rendering reliability

- Improved C64 W/A/S/D/SPACE input reliability and queued-direction movement.
- Corrected software-hires foreground color behavior.
- Improved atomic VIC-II sprite register updates.

## Earlier development

Earlier revisions established software/VIC-II sprite editing, animations, objects, reusable room instances, multi-action Visual Logic, rooms, collision, custom tile properties, named paths, Kick Assembler generation, and editable examples.
