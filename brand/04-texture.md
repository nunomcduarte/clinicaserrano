# Background Texture

The single most distinctive visual cue of Clínica Serrano is the **warm paper background with visible grain**. It runs full-bleed under every layout in the system observed so far. Without it the brand collapses into generic minimalism.

## What it looks like

- Base color: `--color-paper` (~`#B0A695`, warm greige).
- Grain: irregular, low-frequency speckle reminiscent of recycled cardstock or kraft. Not the regimented dot pattern of a halftone.
- Subtle directional fibers visible at high zoom — feels organic, not procedural.
- Contrast of grain vs. base is **low** — it must read as texture, not noise.

## How to reproduce

Two acceptable production routes, in order of preference:

1. **Scanned paper.** A flatbed scan of warm-grey textured cardstock, color-corrected to the paper hex. This is what the original assets look like. Keep the file as a high-resolution greyscale layer that gets multiplied or overlaid on the flat color.
2. **Generated.** Procedural noise + a subtle paper-fiber filter. Acceptable as a fallback (e.g. for the website where loading a high-res scan is wasteful), but never use Photoshop's default noise or Gaussian noise alone — the grain has to feel directional and warm.

## Where it goes

- Always full-bleed, edge to edge.
- Never cropped into a panel, card, or container.
- Never blurred or vignetted.
- Density should not vary across a slide; it's a single uniform texture.

## Where it does *not* go

- Not on the wordmark.
- Not on the headline type.
- Type sits *on* the paper, not on a clean panel placed on top of it.

## Web/digital reproduction

For the website, signage, or anywhere the texture needs to render at varying sizes:

- Export a **seamlessly tileable 1024×1024 PNG** of the texture at 8-bit, ~80–120 KB.
- Apply as a CSS `background-image` with `background-color: var(--color-paper)` underneath, so the base color is correct even before the texture loads.
- For high-DPI: provide a 2× variant; lazy-load if the texture is below the fold.

## Open question

The Instagram exports show a single texture used across all 8 slides — so it appears to be **one fixed texture**, not eight unique scans. Confirm with the original designer; if it is a single asset, it should be checked into this repo as `brand/assets/paper-texture.png` once we have the source file.
