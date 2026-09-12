# Spot Gloss Studio

One board for Mac Safari and Windows Chrome. Site: https://spot-gloss-studio.vercel.app

Do not email a .html file. Safari will show source. Send the website.

Place SVG keeps Illustrator cubics. Image Trace is a draft. Pen owns the plate. Export Plates → zip in Downloads.

## Canvas debug (Safari)

Open https://spot-gloss-studio.vercel.app/?debug=1 or press ` (backtick) on the board.

The overlay reports:
- draw ms and peak (green < 8, amber < 16, red over budget)
- paint fps of real requestAnimationFrame draws (idle should be 0 after the last gesture)
- art vs pack path counts and dense traces (>80 anchors)
- hit-test count and ms on the identity 8×8 ctx
- Retina backing store vs the 3840px Safari cliff
- undo / redo snapshot depth

Then Safari → Develop → Show Web Inspector → Timelines. Record a pan, pinch, or Image Trace. Read Layout & Rendering (green paint of `#view`) and JavaScript & Events → Call Trees → Inverted for `draw` / `walk` / `hitSilhouette`.
