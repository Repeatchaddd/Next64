# Next64 C64 Game Creator VER 17.0

VER 17.0 expands Next64 with integrated SID audio authoring and music playback.

## Highlights

- SID sound-effect editor
- Triangle, saw, pulse, and noise waveforms
- Frequency, ADSR, pulse-width, and duration controls
- Three-voice music pattern editor
- Note/rest rows, tempo, and looping
- Editor audio previews
- Play Sound, Play Music, and Stop Music Visual Logic actions
- Generated C64 SID runtime in `generated_audio.asm`
- Audio resources saved inside `.n64game` projects
- Updated VER 17.0 Quick Start PDF

## Compatibility

Existing projects remain supported. Projects without audio resources continue to load and generate normally. The standard C64 build does not require an REU.

## Testing status

- Python source passed syntax compilation.
- A complete test ASM folder was generated with the new audio runtime and project format.
- The release ZIP passed archive-integrity and required-file checks.
- The Quick Start PDF was rendered and visually checked.
- Final generated games should still be compiled and tested in VICE or on real hardware.

## Current audio limits

Music uses note/rest pattern rows and a shared frames-per-row tempo. Instrument changes, filters, slides, vibrato, and imported SID songs remain future expansion targets. Sound effects use SID voice 1 while music uses all three voices.
