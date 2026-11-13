# Orbit Cat — episode 001

A tiny browser game for the video **I sent my cat into space. Git brought her back.**

## Play

Download this repository as a ZIP, extract it and open `index.html` in a modern browser.
Press Space or click Jump. No account, package install, AI subscription or build step is required.
You can also serve the folder with `python3 -m http.server 8000` and open http://localhost:8000.

## Match the video

- Release tag: `episode-001-v2`.
- Original working checkpoint: `2b5c2be7afd1bca156452e37a93577808fecc0d2`.
- `index.html` and `config.js` are byte-identical to that checkpoint.
- The video deliberately changes `jumpStrength` from 420 to 8400, then restores 420.
- That multiplies initial upward velocity by twenty, not jump height. Gravity stays 1100.
- Video gameplay is a deterministic replay of the actual game, not an AI chat recording.

## Try the experiment

Make a copy before editing, or use Git if it is installed. In `config.js`, change 420 to 8400
and refresh the page. The cat leaves the screen. Restore 420 and refresh to bring back the
original jump. With a Git clone, this command restores just that file from the demonstrated checkpoint:

```sh
git restore --source=2b5c2be7afd1bca156452e37a93577808fecc0d2 -- config.js
```

This discards your local edits to `config.js`; keep anything you want before running it.
Git records commits locally. GitHub hosts the history you upload. An unrecorded version
cannot be recovered from a history that never contained it; other backup tools are separate.

## Prompt recipe

> Multiply jump strength by twenty. Change only that number. Show the difference.

This is an example request, not a transcript of a recorded AI interaction. Inspect the diff
and run the game to check the result. Work out with a parent which online tools you are eligible to use.

The drawing and game code are original. License: MIT. No tracking, network requests or third-party assets.
