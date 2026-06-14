# Social Preview (OG image) spec

GitHub's social preview image appears when the repo URL is shared on Twitter,
LinkedIn, Slack, Discord, and search results. It is **the single highest-leverage
piece of marketing** for an open-source project.

Upload at: **Settings → General → Social preview → Upload an image**.

## Spec

- **Dimensions:** 1280 × 640 px (2:1 aspect ratio, GitHub's required size)
- **File:** PNG or JPG, ≤ 1 MB
- **Safe zone:** keep critical text within the inner 1100 × 500 region — LinkedIn/Twitter can crop edges

## Design brief

A clean, technical, slightly futuristic feel — matches the "lab" metaphor.

**Background**
- Deep navy → indigo gradient (`#0F1226` → `#1E1B4B`)
- Subtle grid or hex pattern at 5–8% opacity
- Optional: faint Python `>>>` glyphs or `O(log n)` annotations as wallpaper

**Foreground (left half)**
- Logo / wordmark: **OCTALUM·PYLAB** in a bold geometric sans (Space Grotesk Bold or Inter ExtraBold), white, ~96px
- Tagline directly below: **"Master Python DSA through guided experimentation"** in 32px, soft white (`#E2E8F0`)
- Small caption: **"8 phases · 11 patterns · Big-O annotated · Tested"** in 24px, indigo accent (`#A5B4FC`)

**Foreground (right half)**
- A stylized representation of the 8 phases: 8 numbered hexagons or rounded squares in a curved chain, each containing the phase number, colored on a gradient from teal (`#14B8A6`) at Phase 1 to magenta (`#D946EF`) at Phase 8
- Or alternatively: a minimal binary-tree / graph diagram in cyan strokes

**Footer band**
- `github.com/Harery/LuminaPy` in monospace (JetBrains Mono), 22px, `#94A3B8`
- A small Python logo and an MIT/GPLv3 badge in the corner

## Quick way to produce it

The fastest path is to ask a generative image model with this prompt:

> A 1280×640 GitHub social preview banner. Deep navy gradient background with a faint hex grid. Left side: large white wordmark "OCTALUM·PYLAB" in a bold geometric sans, with the tagline "Master Python DSA through guided experimentation" below in soft white, and a small indigo subline "8 phases · 11 patterns · Big-O annotated · Tested". Right side: a chain of 8 numbered hexagons arranged in a gentle S-curve, gradient teal→magenta. Footer: monospace URL `github.com/Harery/LuminaPy` in muted slate. Modern, technical, slightly futuristic. No people. No clutter.

Alternative: do it in Figma in 20 minutes — a free template is at https://www.figma.com/community/file/1080434957197582165 (GitHub OG template).

## Once uploaded

After uploading, force-refresh the Twitter / LinkedIn caches:

- Twitter card validator: https://cards-dev.twitter.com/validator
- LinkedIn post inspector: https://www.linkedin.com/post-inspector/
- Open Graph debugger: https://opengraph.dev/
