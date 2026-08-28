# Contributing to Next64

Thank you for helping improve Next64 C64 Game Creator.

The project is still evolving quickly, so the most valuable contributions are reproducible bug reports, small focused fixes, documentation improvements, and example projects created entirely with normal editor features.

## Reporting a bug

Use the Bug Report issue template and include:

- Exact Next64 version
- Windows and Python versions
- Software or VIC-II renderer
- Hires or multicolor mode
- Clear steps to reproduce
- What you expected
- What actually happened
- Whether it occurs in editor Test Play, generated code in VICE, or both
- Full Kick Assembler error text when compilation fails
- A small `.n64game` project when possible

Please report one underlying problem per issue. Separate reports make testing and version tracking much easier.

## Suggesting a feature

Describe the general-purpose capability rather than only one hard-coded game. Explain:

- What a game creator needs to accomplish
- Why existing actions or conditions cannot accomplish it
- What editor controls would be needed
- What C64 runtime behavior it should generate
- Any expected memory or performance cost

Features should remain useful across multiple game genres whenever practical.

## Code contributions

Before preparing a pull request:

1. Base changes on the newest public version.
2. Keep the editor compatible with existing `.n64game` projects.
3. Avoid hard-coding behavior for one example game.
4. Keep standard-memory projects working without an REU.
5. Preserve VIC-II color indices even if editor preview colors change.
6. Test editor loading, project save/reload, ASM generation, and ZIP contents.
7. Test generated code with Kick Assembler and VICE when the change affects runtime output.
8. Update the README, changelog, and Quick Start when behavior changes.

## Pull requests

A pull request should explain:

- The problem being solved
- The chosen implementation
- Compatibility considerations
- Tests performed
- Known remaining limitations

Avoid mixing unrelated fixes into one pull request.

## Project files and examples

Examples must be constructible and editable through the normal Game Creator tools. Do not add examples that depend on hidden, example-specific runtime rules.

## Conduct

Be patient, specific, and respectful. Critique the implementation or design, not the person reporting or contributing it.
