# Comparison and choosing

The right format follows from what the image is: a photograph, a graphic with sharp edges or transparency, an animation, or a scalable logo. The table below summarizes the common formats, and the guidance after it turns that into simple decisions.

## Quick comparison

| Format | Compression | Transparency | Animation | Type | Best for |
|--------|-------------|--------------|-----------|------|----------|
| JPEG | Lossy | No | No | Raster | Photographs, broad compatibility |
| PNG | Lossless | Full alpha | No (APNG only) | Raster | Graphics, screenshots, transparency |
| GIF | Lossless | Binary only | Yes | Raster | Legacy simple animation (mostly obsolete) |
| WebP | Lossy or lossless | Full alpha | Yes | Raster | Modern default for photos and graphics |
| AVIF | Lossy or lossless | Full alpha | Yes | Raster | Smallest photos, high dynamic range |
| SVG | Lossless (vector) | Full alpha | Yes (via CSS/JS) | Vector | Logos, icons, diagrams |

## A decision guide

- Is it a logo, icon, or diagram made of shapes and text? Use SVG.
- Is it a photograph? Prefer AVIF or WebP for size, with a JPEG fallback. Plain JPEG is fine when you need maximum compatibility with no fallback setup.
- Is it a graphic with sharp edges, flat color, or transparency (screenshots, UI, illustrations)? Use WebP lossless, or PNG when you need a universally supported lossless file.
- Does it need animation? Use an animated WebP or AVIF, or better yet a real video file. Avoid GIF except where a platform forces it.

## Practical tips

Serve modern formats with fallbacks using the `<picture>` element so you get small files without breaking older clients. Compress deliberately: for lossy formats, pick the lowest quality that still looks good, since the last few quality points cost a lot of bytes for little visible gain. Always size images to the dimensions they are actually displayed at rather than shipping a huge original and shrinking it in the browser. And keep an `alt` attribute on every meaningful image, both for accessibility and because it is the text shown if the image ever fails to load.
