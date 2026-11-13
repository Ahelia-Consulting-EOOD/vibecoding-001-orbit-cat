# Orbit Cat — The Snack Mission

Original browser game for the full Episode 001. Open `index.html` in a modern browser. No account, packages, network access or build step is needed.

Press Space or Jump to catch the floating snack and land on the launchpad. Press R or Retry for another attempt. The two mission checks report collection and landing separately.

`config.js` contains `jumpStrength`, the initial upward speed in pixels per second. The working value is 420. The episode deliberately tests 8400, restores the working file from a Git checkpoint, then compares 560. These values are speeds, not heights; gravity stays at 1100 pixels per second squared.

This new game was AI-authored in the recorded 13 November 2026 production run. It is distinct from the earlier pilot fixture. Shapes are original, fonts are system fonts, and the game sends no data anywhere.

## Repeatable checks

For capture/testing, set `game.manual = true`, call `game.reset()`, then `game.jump()` and repeated `game.step(1/60)`. `game.snapshot()` reports time, position, velocity, snack collection and landing. Normal play uses real time. The simulation uses small discrete time steps, so results are compared with equivalent inputs rather than an ideal continuous-physics formula.
