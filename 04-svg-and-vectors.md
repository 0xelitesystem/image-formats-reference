# SVG and vectors

SVG (Scalable Vector Graphics) is fundamentally different from the other formats: instead of storing pixels, it stores shapes as mathematical instructions in a text based format. This means it scales to any size with perfect sharpness and stays tiny for simple graphics, which makes it the right choice for logos, icons, and diagrams, and the wrong choice for photographs.

## Why vectors are different

A raster image is a fixed grid of pixels, so enlarging it past its native resolution makes it blurry. An SVG describes an image as instructions like "draw a circle here, fill this path with that color," so the browser redraws it crisply at any size, from a favicon to a billboard, with no quality loss. Because the file describes shapes rather than millions of pixels, a logo as SVG is often far smaller than the same logo as PNG.

## What SVG looks like

An SVG is human-readable markup you can open in a text editor:

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
  <circle cx="50" cy="50" r="40" fill="#d4003e" />
  <text x="50" y="56" text-anchor="middle" fill="white">OK</text>
</svg>
```

Being text, SVG can be styled with CSS, animated, made interactive with scripting, and it stays sharp on any screen density.

## Where SVG wins and where it does not

SVG is ideal for logos, icons, illustrations, charts, and diagrams: anything made of shapes, lines, and text that should scale cleanly. It is the wrong tool for photographs, because a photo is not made of simple shapes; describing every subtle pixel as a shape would produce an enormous, impractical file, so photos must be raster (JPEG, WebP, AVIF). There is also a security note: because SVG can contain script, SVGs from untrusted sources should be sanitized before being served, since a malicious SVG can carry active content. For your own logos and icons, though, SVG is the clear best choice.
