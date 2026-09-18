# Peg Solitaire

A classic 33-hole peg solitaire game — a single self-contained HTML file, playable in any browser and installable to a phone home screen.

**Play it live:** https://guri-ai-70.github.io/Peg-Solitaire/

## How to play

The board has 33 holes with 32 pegs, one empty hole in the centre. Tap a peg to select it — reachable holes will glow and pulse. Tap a glowing hole to jump: the peg jumps over a neighbouring peg into the empty hole, and the peg it jumped over is removed.

Goal: keep jumping until only **one peg remains**, ideally in the centre hole.

Rows and columns are labelled chess-style — columns **A–G** along the bottom, rows **1–7** down the left side — so any position can be described the same way as a chess square (e.g. "D4" is the centre hole).

## Features

- **Undo** — step back one move at a time
- **New game** — reset the board to the starting position
- **Settings (gear icon)** — choose a board colour (Walnut, Ebony, Forest, Slate, Cherry) and a peg style (Wood, Marble, Gold)
- **Solve** — password-protected (intended for a parent/host to reveal on request, not for casual browsing). Enter the password, then choose:
  - **View** — watches a full 31-move solution play out automatically on the board, one jump at a time, ending with a single peg in the centre
  - **Print** — shows the same 31 moves as a numbered table (in chess notation, e.g. "D6 → D4") and opens the browser's print dialog so it can be printed or saved as a PDF

## Mobile installation

Open the live link above in a mobile browser (Chrome/Safari), then use the browser menu's **"Add to Home Screen"** option. The game opens full-screen, like an installed app, with its own icon.

## Technical notes

- Single file: `index.html` — no build step, no dependencies, no external assets
- Hosted via GitHub Pages, served directly from the `main` branch
- The embedded 31-move solution was computed and verified with a brute-force solver, confirming every move is legal and the sequence ends with exactly one peg in the centre hole
