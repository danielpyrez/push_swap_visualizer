# Push Swap Visualizer

An interactive, single-file visualizer for the classic **push_swap** stack-sorting
algorithm exercise. Load a series of numbers into Stack A, run or step through
`sa`, `pa`, `ra`, `rra`, `sb`, `pb`, `rb`, `rrb`, `ss`, `rr`, `rrr` moves, or just
drag blocks around by hand to build your own sequence.

This project was built collaboratively with [Claude](https://claude.ai) (Anthropic).

## Features

- **Two stacks (A and B)** rendered as columns of bars, sized proportionally to
  each value, with a live block count next to each stack's title.
- **Drag & drop** — grab any block and drop it into a specific slot in either
  stack, or drop it in empty space to set it free. Right-click a block to edit
  its number or delete it. Drag onto the trash icon to remove it.
- **Load a series** — type or paste numbers into the input box (spaces, commas,
  semicolons, or even a pasted `{1, 2, 3}` array all work), or generate a
  random shuffled series of N blocks.
- **Copy the current Stack A** — as a `{x, y, z}` array or as a plain
  space-separated `x y z` list, ready to paste elsewhere.
- **Simulate moves** — type a sequence of push_swap operations (e.g. `pb sa rr`)
  and play, pause, resume, or reset the simulation, with an adjustable speed
  slider (0.5 ms up to 1000 ms per step) and a live step counter.
- **Manual operations bar** — click any operation button directly to apply a
  single move at a time.
- **Adaptive layout** — blocks automatically compress (vertically first, then
  horizontally) as the stacks grow, so everything always stays in view, up to
  a safety cap of 300 blocks.

## Getting started

This is a single self-contained HTML file — no build step, no dependencies.

1. Download `index.html` and `icon.svg` and keep them in the **same folder**
   (the favicon is loaded as a relative path).
2. Open `index.html` in any modern browser.

## Usage tips

- **Load a series:** type numbers into the left input (e.g. `3 8 1 9 4`) and
  click "Load into Stack A", or press Enter.
- **Randomize:** set a count and click "🎲 Randomize" to shuffle a fresh
  series of that size into Stack A.
- **Simulate:** type a move sequence into the right input (e.g. `pb pb sa rr`)
  and press ▶ to run it step by step at the chosen speed. Use ↺ to reset back
  to the last loaded series.
- **Copy:** use the `{}` button to copy Stack A as `{x, y, z}`, or the
  clipboard icon to copy it as `x y z`.

## Tech stack

Plain HTML, CSS, and vanilla JavaScript (no frameworks, no build tools).
Fonts are loaded from Google Fonts (Space Mono, Work Sans).

## License

Feel free to use, modify, and share this project.