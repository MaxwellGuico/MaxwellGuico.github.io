# Maxwell Guico · Portfolio

Static site for GitHub Pages: no build step.

- `index.html`: the whole site. Edit the `PROJECTS` array near the bottom to change project text.
- Diagrams: the "how it works" SVG for each project is drawn by the `DG` script inside `index.html`. (`assets/diagrams.js` is an older copy you can delete.)
- `assets/videos/`: put demo videos here (see below).
- `assets/`: Geist font (SIL OFL).
- `.nojekyll`: tells GitHub Pages to serve files as-is.

## Videos
Drop these files in `assets/videos/`. Each appears on its project page automatically, and stays hidden if the file is missing:
- `wave-rover.mp4`
- `apriltag-drone.mp4`
- `bingda-ros.mp4`

Use H.264 MP4 and keep each under ~25 MB (GitHub rejects files over 100 MB). To shrink one:
`ffmpeg -i in.mov -vf scale=1280:-2 -c:v libx264 -crf 28 -preset veryfast -an out.mp4`

## Publish
1. Create a repo named `MaxwellGuico.github.io`.
2. Push these files to the root of `main`.
3. Settings → Pages → Deploy from branch → `main` / root.
Site goes live at https://maxwellguico.github.io
