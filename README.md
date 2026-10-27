# Grid Grader

A browser-based site grading tool for landscape architects, by BOLD (Ben Orbach Landscape Design).

Import a DXF survey and proposed plan, outline the grading area, and shape the ground on an adjustable grid or directly on your design linework. Slopes, contours, cut/fill and a live 3D model update as you work.

## What it does

- **DXF import**: reads existing spot elevation text (TEXT, MTEXT, attributes, multileaders) by layer, snaps values to their point symbols, and lets you pick the grading area from a closed polyline.
- **Existing vs proposed**: existing grades stay locked outside the grading area; inside, the surface starts at existing grade and follows the spots you set.
- **Adjustable grid**: any block size, rotation and origin, with E–W and N–S slopes and flow direction for every block.
- **Proposed plan underlay**: design linework drapes on the graded surface in 3D. Set elevations on its corners (the surface passes exactly through them, even between grid points) or grade a whole line or shape at once.
- **3D editing**: click and drag points up or down in the 3D model; surrounding interpolated points follow live.
- **Analysis**: slope classes by area (editable breaks; defaults 1, 2, 5, 8.33 and 33.3 %), contours, cut, fill and net volumes.
- **Export**: AutoCAD R12 DXF of proposed spots, grid points, contours and grading limit, in the drawing's original units and coordinates; CSV of all grid points; project files you can save and reopen.

## Running it

It's a single static page: `index.html`. Open it in a browser, or host it anywhere that serves static files. Work is saved in the browser automatically; use **Save / load** to download a project file.

Three.js, OrbitControls and Delaunator load from public CDNs.

## Notes

- DWG files can't be read in a browser; save as DXF (ASCII) from AutoCAD first.
- Elevations are sampled at grid points, so use a smaller block size where fine detail matters.
