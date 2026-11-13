# Image Formats

A plain-language reference on the image formats used on the web: JPEG, PNG, GIF, WebP, AVIF, and SVG. It covers the concepts that separate them (lossy versus lossless, transparency, animation, raster versus vector), what each format is good at, a quick comparison table, and practical guidance on choosing the right one for a given image.

## The core idea

There is no single best image format; each is a tradeoff between file size, quality, transparency, animation, and browser support. Photographs compress smallest with lossy formats (JPEG, or the newer WebP and AVIF), while graphics with sharp edges and flat color, or anything needing transparency, do better with lossless formats (PNG, or again WebP), and logos and icons that must scale cleanly belong in SVG. The modern default is to serve WebP or AVIF for their smaller sizes and fall back to JPEG or PNG where needed.

## What is inside

- [01-core-concepts.md](01-core-concepts.md) lossy vs lossless, transparency, animation, raster vs vector.
- [02-the-classic-formats.md](02-the-classic-formats.md) JPEG, PNG, and GIF.
- [03-the-modern-formats.md](03-the-modern-formats.md) WebP and AVIF.
- [04-svg-and-vectors.md](04-svg-and-vectors.md) why SVG is different and where it wins.
- [05-comparison-and-choosing.md](05-comparison-and-choosing.md) a comparison table and a decision guide.

## The stance

This reference favors picking the format that fits the image rather than defaulting to one for everything. It treats WebP and AVIF as the sensible modern choice for photos and graphics with fallbacks, JPEG and PNG as reliable baselines, GIF as largely obsolete for its original uses, and SVG as the correct home for logos, icons, and diagrams.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright RBL Industries LLC 2026.
