# Core concepts

Choosing an image format comes down to a few underlying properties: whether compression is lossy or lossless, whether the format supports transparency, whether it supports animation, and whether it stores the image as pixels (raster) or as instructions (vector). Every format is a particular combination of these, so understanding the concepts lets you predict which format fits.

## Lossy versus lossless

Lossy compression permanently discards some image data to make the file smaller, accepting a quality loss that is often invisible at normal viewing. JPEG, and the lossy modes of WebP and AVIF, work this way and are excellent for photographs, where small imperfections do not matter and the size savings are large. Lossless compression shrinks the file without throwing anything away, so the decoded image is identical to the original. PNG, GIF, and the lossless modes of WebP are lossless, which suits graphics with sharp edges, text, and flat color where any lossy blur would be obvious. Repeatedly re-saving a lossy image degrades it each time; lossless images can be re-saved freely.

## Transparency

Transparency lets parts of an image be see-through so a background shows behind it. Two kinds exist: full alpha transparency, where each pixel can be any level of opacity (smooth edges over any background), and binary transparency, where a pixel is either fully visible or fully invisible (which gives jagged edges). PNG, WebP, AVIF, and SVG support full alpha. GIF supports only the binary kind. JPEG supports no transparency at all, which is its main limitation for graphics.

## Animation

Animation means multiple frames stored in one file that play in sequence. GIF is the classic animated format but is limited to 256 colors per frame and produces large files. WebP and AVIF also support animation with far better compression and full color, which is why an animated WebP or a real video usually beats an animated GIF. PNG animates only through the less-supported APNG variant.

## Raster versus vector

Raster images (JPEG, PNG, GIF, WebP, AVIF) are grids of pixels, so enlarging them past their resolution makes them blurry or blocky. Vector images (SVG) store shapes as mathematical instructions, so they scale to any size with perfect sharpness. Photographs must be raster; logos, icons, and diagrams are ideal as vectors.
