# The modern formats

WebP and AVIF are newer web image formats designed to produce much smaller files than JPEG and PNG at comparable quality, while supporting transparency and animation in one format. They are the current recommended defaults for most web images, served with a JPEG or PNG fallback for the rare browser or tool that cannot read them.

## WebP

WebP is a versatile format that supports both lossy and lossless compression, full alpha transparency, and animation, all in a single format. In lossy mode it typically produces files noticeably smaller than an equivalent JPEG; in lossless mode it usually beats PNG on size too. Because one format covers photos, graphics with transparency, and animation, WebP can replace JPEG, PNG, and GIF in most situations. Browser support is now effectively universal across current browsers. WebP is a strong, safe default: use it for photographs, for graphics needing transparency, and in place of animated GIFs.

## AVIF

AVIF is a newer format based on modern video compression that generally achieves even smaller files than WebP, especially for photographs, and supports transparency, animation, and a wider color range including high dynamic range. Its compression is the best of the common web formats, so for large photographic images AVIF can save the most bandwidth. The tradeoffs are that encoding can be slower and support, while good in current browsers, arrived later than WebP, so a fallback still matters. Use AVIF when squeezing photographic file size to the minimum is the priority and you can provide a fallback.

## Serving them with fallbacks

Because a small number of older clients may not support these formats, the standard pattern serves a modern format first and falls back automatically:

```html
<picture>
  <source srcset="photo.avif" type="image/avif">
  <source srcset="photo.webp" type="image/webp">
  <img src="photo.jpg" alt="A description of the photo">
</picture>
```

The browser picks the first format it understands, so modern browsers get the small AVIF or WebP while older ones get the JPEG. This gives you the size savings with no risk of a broken image, which is why it is the recommended approach.
