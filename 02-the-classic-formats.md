# The classic formats

JPEG, PNG, and GIF are the three long-established web raster formats, each built for a different job: JPEG for photographs, PNG for graphics and transparency, and GIF originally for simple animations and limited-color images. They are universally supported, which is why they remain safe baselines even as newer formats overtake them on size.

## JPEG

JPEG is a lossy format built for photographs and other images with smooth gradients and many colors. It compresses continuous tone images very efficiently by discarding detail the eye barely notices, and you can choose a quality level to trade size against fidelity. Its weaknesses are clear: it has no transparency, and it handles sharp edges, text, and flat color poorly, producing visible "artifact" halos around hard lines. Use JPEG for photos when you need broad compatibility; avoid it for logos, screenshots of text, or anything needing a transparent background.

## PNG

PNG is a lossless format built for graphics, screenshots, and images needing transparency. Because it is lossless, edges and text stay crisp and re-saving never degrades it, and it supports full alpha transparency for smooth edges over any background. The tradeoff is size: for a photograph, a PNG is much larger than an equivalent JPEG, because lossless compression cannot match lossy on complex imagery. Use PNG for logos, icons, screenshots, diagrams, and anything with sharp edges or transparency. Do not use it for large photographs unless you specifically need losslessness.

## GIF

GIF is a lossless format limited to a 256-color palette, historically used for simple animations and small flat-color graphics. Its defining features are animation support and binary (on or off) transparency. Today it is largely outclassed: for still images PNG is better, and for animation WebP, AVIF, or an actual video file are dramatically smaller and support full color. The 256-color limit makes GIF poor for photographs, and animated GIFs are notoriously heavy. Reach for GIF only when a specific platform requires it; otherwise prefer the modern alternatives.
