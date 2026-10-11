# Tessera

An 8×8 block puzzle for phones. Drag pieces onto the slab, fill rows and columns to clear them, and keep a streak going.

**Play:** https://perpetualpixel.github.io/GemDev/

On a phone, open the link and use your browser's "Add to Home Screen" to launch it full screen like an app.

## Rules

- Drag any of the three pieces onto the board. Pieces do not rotate.
- A full row or column clears. Several can clear at once.
- Clear again within three placements to keep a streak. The streak multiplies line points.
- Three new pieces arrive once all three are placed.
- The game ends when none of the remaining pieces fits.

| Action | Points |
| --- | --- |
| Each tile placed | 1 |
| 1 / 2 / 3 / 4 lines at once | 10 / 30 / 60 / 100 × streak |
| Empty the whole board | +300 |

## How it is built

The whole game is `index.html`: markup, styles and script in one file, with no build step and no dependencies. The only outside request is for two Google Fonts, and the game falls back to system fonts without them.

- `index.html` is the game.
- `manifest.webmanifest` and the icon files make "Add to Home Screen" work.
- `.nojekyll` tells GitHub Pages to serve the files as they are.

Scores and the game in progress are saved in the browser's local storage on each device.

To run it locally, open `index.html` in a browser, or serve the folder with `python3 -m http.server`.
