# Background treatments

Choose by product character, content density, and rendering budget. The suggestions below are starting points, not fixed industry assignments. Preserve the user's requested aesthetic when it remains usable.

## Select a treatment

Start with the region's content and the existing imagery. Identify the treatment's job: separate sections, frame product evidence, reinforce brand character, or establish atmosphere. If imagery and typography already provide the needed emphasis, choose a plain surface.

For a selected treatment, decide:

- **Placement:** locate the focal area and the quiet zone behind reading and actions. Keep decorative contrast subordinate to the intended focal point.
- **Fit:** use the existing palette and motifs. A treatment that depends on a new palette or replacement imagery requires that scope to be authorized.
- **Delivery:** choose CSS/SVG for simple geometry and optimized raster assets for material detail. Prefer a static asset when animation adds no useful feedback.
- **Adaptation:** specify how the region behaves on narrow screens, with reduced motion, and before or without its decorative asset. A solid base surface should keep text and controls usable when decoration fails to load.

Evaluate candidates against the actual content, rather than choosing a treatment by industry label. Keep these decisions brief; a separate specification is unnecessary.

## Treatment palette

| Treatment | Useful character or placement | Implementation and restraint |
| --- | --- | --- |
| Felt texture | Soft, tactile, comforting surfaces | Use a subtle tiled raster; keep fibers low contrast and away from fine text. |
| Fluted glass | Architectural depth, layered product reveals | Use a static ribbed asset or restrained masked distortion; place readable content on an undistorted layer. |
| Thermal gradients | Energy, experimentation, expressive focal points | Limit hot color areas; contain intense transitions to a focal region and check contrast locally. |
| Water ripples | Calm, reflection, fluidity | Prefer a still image or subtle isolated animation; keep readable content on a stable surface. |
| Speckled graphite | Technical craft, monochrome editorial depth | Tile fine irregular speckles; separate texture from small labels to prevent visual noise. |
| Single-hue landscapes | Atmosphere, quiet scale, a strong color identity | Tint a landscape with a unified palette; reserve negative space for copy and plan mobile crops. |
| Blueprint grids | Precision, systems, building and planning | Use low-contrast CSS/SVG lines; emphasize a few meaningful alignments rather than decorating every cell. |
| Halftone | Print, retro energy, graphic contrast | Use controlled dot scale and masks; test scaled exports for moiré and keep dots outside body copy. |
| Grainy gradients | Warmth and depth in otherwise smooth fields | Layer a small static noise tile over a restrained gradient; avoid expensive per-frame noise generation. |
| Grass texture | Nature, play, tactile outdoor character | Use intentional photography or a cutout with quiet text space; avoid a busy full-page repeat. |
| Dithered images | Computational, nostalgic, deliberately limited palettes | Preprocess imagery; retain silhouette and subject recognition and test at the rendered size. |
| Paper texture | Editorial, handmade, warm reading surfaces | Use a subtle tile or scan, adjusting base color and contrast together; preserve clean form controls. |
| Contour lines | Terrain, exploration, analytical flow | Use sparse SVG contours with controlled density; avoid tangles around headings and CTAs. |
| Cloud sky | Air, optimism, spaciousness | Plan image crops and a stable text scrim; keep bright clouds from erasing light text. |
| Pixel mosaics | Modular creativity, playful computation | Use a limited palette and purposeful clusters; keep tiny cells away from small text. |
| Lens distortion | Optical experimentation, a dramatic focal object | Distort decorative artwork only; prefer a baked asset when real-time distortion adds little value. |
| Stippled gradients | Soft shading with a drawn or printed finish | Vary dot density gradually in a static asset; inspect compression and banding at final scale. |
| Square-dot grids | Order, modularity, technical rhythm | Use a repeating CSS/SVG pattern at low contrast; avoid high-frequency aliasing on mobile. |
| Blurred photos | Context and atmosphere without literal detail | Use a preblurred optimized image where practical; ensure the source still supports the product story. |
| Iridescent shapes | Optical richness, premium or futuristic objects | Contain hue shifts to a few shapes against a quiet base; keep CTA color distinct. |
| Impressionist paintings | Artistic warmth, human texture, expressive color | Use licensed or generated artwork with a suitable crop; separate dense brushwork from reading areas. |
| ASCII and pixels | Developer culture, computational play, retro systems | Use decorative SVG/raster or an aria-hidden layer; provide real semantic text for meaningful information. |

## Combining treatments

Select a base and an accent with different jobs. Good starting pairs include paper + sparse halftone, blueprint grid + one iridescent object, single-hue landscape + fine grain, or graphite + a restrained thermal focal point. These are examples, not defaults.

When two effects compete in frequency, contrast, or saturation, reduce one or separate their regions. Establish one focal point; use masks, fades, scrims, or solid content surfaces to protect reading. Carry a shared palette or texture scale across the page. Mobile may need a simpler crop or a static variant.

Inspect the final rendering for text contrast, moiré, tiling seams, compression artifacts, and distracting repetition. If the effect makes the action harder to find, simplify it. Do not add motion merely because a treatment supports it.

## Verify the treatment in context

Inspect the actual region at desktop and mobile widths, including the busiest and brightest parts behind content. Check that the product image retains its meaning and prominence, controls remain easy to locate, and decorations neither intercept input nor create overflow.

Check the static or reduced-motion variant and the asset-loading fallback where applicable. If the treatment competes with the message, first reduce its extent, density, or contrast; use a plain surface if it still obscures the intended hierarchy. Judge the result with real content rather than an empty background preview.
