# batCAD

**Precision in the dark.**

A fast, minimal 2D CAD drafting tool that runs entirely in your browser: one HTML file, no build step, no install. Black canvas, yellow highlights, nothing in the way.

![batCAD on a pure black canvas with a selected rectangle and winged-blade grips](docs/screenshot.png)

## Features

- **Drawing tools:** line, rectangle, circle, arc, polyline, dimension
- **Editing:** select, trim, extend, plus a command line for precise input (rotate, copy, offset, fillet, and more; type `help`)
- **Snaps and constraints:** grid snap, object snap, ortho
- **Layers:** per-layer visibility, locking, dashed linetypes and line weights
- **Units:** work in millimetres or inches; geometry is always stored in mm
- **Grips:** select an object and drag its winged-blade grips to reshape it
- **Export:** save drawings as `.bat` files or export clean `.svg`
- **Touch friendly:** works on phones and tablets as well as desktop

### Keyboard shortcuts

| Key | Tool | Key | Tool |
|-----|------|-----|------|
| `V` | Select | `D` | Dimension |
| `L` | Line | `T` | Trim |
| `R` | Rectangle | `E` | Extend |
| `C` | Circle | `/` | Command line |
| `A` | Arc | `P` | Polyline |

## The look

batCAD is a visual reskin built around a classic dark, noir mood:

- Pure black background with near-black panels (always dark, no light theme)
- Yellow accent for selection, active tools, and the origin axes
- Condensed, uppercase, sharp-cornered controls with a soft glow on hover
- A subtle vignette and a faint city-skyline silhouette along the bottom of the canvas
- A shuriken-bat logo and winged-blade selection grips

## Running it

Open `index.html` in any modern browser. To host it, serve the repository root as static files (for example with GitHub Pages).

## File format

Drawings are saved as `.bat` files. A `.bat` file is plain JSON: `{ "format": "batcad", "version": 1, ... }`.

> **Note for Windows users:** `.bat` is also the extension for Windows batch scripts. These files are data, not scripts. Open them from inside batCAD rather than double-clicking them.

Drawings saved by NinjaCAD (`.nja`, format `ninjacad`) still open in batCAD, and your autosaved NinjaCAD drawing is picked up automatically.

## Credits and origin

batCAD is a **fork of [NinjaCAD](https://github.com/withshalom/ninja)** by Shalom / WithShalom Studios. NinjaCAD is the source of all the drawing, editing, snapping, layer, and file-handling code. batCAD changes the look and feel and a few names; the engine is NinjaCAD's.

Changes from NinjaCAD:

| | NinjaCAD | batCAD |
|---|---|---|
| Name and logo | NinjaCAD, four-point star | batCAD, shuriken-bat mark |
| Theme | Dark and light | Pure black only |
| Accent | Red | Yellow |
| Selection grips | Diamonds | Winged blades |
| File extension | `.nja` | `.bat` |
| Typography | Barlow | Barlow Condensed, uppercase controls |

## License

Copyright © WithShalom Studios. This project is a fork of NinjaCAD; refer to the upstream repository for its terms.
