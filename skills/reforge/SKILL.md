---
name: reforge
description: Redesign landing pages and mobile onboarding flows with intentional typography, composition, background treatments, and clearer conversion paths. Use for landing-page redesigns, visual polish, or onboarding improvements; not general backend work.
---

# Reforge

Make the page feel like the best version of its own brand: recognizable, clearer, more comfortable, and more rewarding to explore. Aim for the owner to feel, “This finally looks like what I had in mind.” Treat that as a design intention, not a guaranteed emotional outcome. Default to a short audit followed by implementation. Offer alternative directions when requested; do not insert a design approval gate into an authorized redesign.

## Establish the direction

Inspect the supplied page, screenshots, design files, or relevant UI code and project instructions. Identify the audience, product promise, primary action, current brand, and implementation constraints. Ask only for missing information that materially changes the result; otherwise state a reasonable assumption and proceed. If no target is supplied or discoverable, ask for one.

Treat existing brand identity and imagery as constraints, including on unfinished pages. A request to redesign, polish, modernize, or make a page less flat authorizes improvements within those constraints; it does not authorize rebranding or removing imagery. Respect the requested scope, existing stack, component library, and working flows. A request for critique produces a critique; a request for implementation produces working changes. Use the runtime's available tools without requiring a specific agent, plugin, or framework.

Identify what already works: the strongest image, distinctive personality, and most compelling message. Preserve and amplify those strengths. Choose an emotional direction grounded in the brand and audience, such as welcoming, calm, playful, confident, or inspiring; ask only if ambiguity would materially change the design.

Conclude the audit with a brief working design brief: the visitor's task, the biggest observed obstacle, the intended visual focal point, and up to three observable improvements. For example: explain the product through the headline and image, make the primary action visually dominant, and keep the product screenshot legible on mobile. Ground these targets in inspected content; label assumptions. Keep the brief in the working response rather than creating a required document or approval gate. Scale it down for narrow edits.

Choose a concrete direction within the existing brand: mood, type hierarchy, composition, and a compatible signature treatment using the current palette. Use the brief to decide which changes earn their place.

## Preserve the brand and imagery

When rendering tools are available, capture before screenshots at representative desktop and mobile viewports for a comparable final presentation. Before editing, capture a brief baseline from the existing page and code: brand color values and their roles, light/dark theme, fonts, logo, voice, and visible images with their locations and purpose. Use this baseline during implementation and final comparison; no extra document is required.

- Keep the existing primary, secondary, and accent colors, theme, logos, brand fonts, and recognizable visual motifs. Improve spacing, hierarchy, sizing, composition, and texture within that identity. Map existing colors to tokens instead of substituting a new palette. For contrast problems, first adjust the surrounding surface or text treatment; propose any necessary change to a brand color rather than silently replacing it.
- Retain existing images, illustrations, product screenshots, and image-bearing sections. Improve framing, responsive sizing, compression, and placement while preserving subject, meaning, and prominence. Moving an image must not effectively remove it through hiding, extreme cropping, tiny sizing, obscuring overlays, or loss on mobile. Background effects supplement existing imagery rather than replace it.
- Preserve the brand's tone, terminology, positioning, and personality when editing copy. Improve clarity without turning distinctive language into a generic marketing voice.
- Change brand identity, replace assets, or remove images only when the user explicitly requests or authorizes that specific scope. If a removal or rebrand would help, propose it separately and continue the authorized improvements. Do not treat an unfinished design, aesthetic preference, broken asset, or performance concern as permission to discard existing identity or imagery; repair or flag asset issues.
- Use creative freedom for genuinely unspecified elements. If starting from a blank page with no brand or assets, establish a direction from the brief.

## Build the redesign

Prioritize the changes with the greatest visible benefit: typography, spacing, hierarchy, and image framing before decorative effects. Create one memorable moment from the brand's own material, such as a beautifully framed product image, expressive headline, subtle texture, or useful interaction. This can be quiet; delight does not require animation or spectacle. Carry the same care through lower sections, forms, mobile layouts, and interaction states within the requested scope.

### Message and composition

Read [Composition](references/composition.md) when choosing or changing page layout, section hierarchy, image scale, or responsive reading order. Use the content and visitor task to choose the structure.

- Make the first screen explain the product, intended audience, and useful outcome. Give the primary action a specific label and supporting context where needed.
- Rewrite headlines, supporting copy, and CTAs when they improve clarity. Preserve factual meaning and the existing brand voice. Use supplied evidence for testimonials, metrics, logos, pricing, and guarantees; never invent social proof.
- Organize the page around the visitor's decision: promise, product evidence, benefits, objections, and action. Improve the order and presentation of existing sections without silently dropping their content or imagery. For new sections, include only those that earn their place; this is not a mandatory section template.
- Create hierarchy through scale, whitespace, alignment, contrast, and deliberate changes in density. Use real product imagery or an accurate demonstration where it explains value. Keep forms, links, analytics hooks, and interaction states working.

### Typography and color

- Define explicit display, heading, body, label, and supporting-text roles using a small token system. Keep existing brand font families and refine their hierarchy; choose new families only where none are established or a typography change is explicitly authorized.
- Choose type for both character and reading conditions. Tune weight, tracking, line height, and measure together. Start body copy around 16–18 CSS px and 45–75 characters per line, then adapt to the content and platform. Use fluid heading sizes with sensible bounds and intentional wrapping.
- Test long headlines, real copy, small screens, text enlargement, and font fallbacks. Keep essential content visible at 200% zoom and avoid layouts that depend on one exact line break.
- Map the existing palette to semantic roles: canvas, surface, text, muted text, accent, border, focus, and status. Check text contrast against the actual rendered background, including its lightest and darkest regions.

### Depth and backgrounds

Read [Background treatments](references/backgrounds.md) when selecting or implementing texture, atmosphere, imagery, grids, or optical effects. It contains selection criteria, a 22-treatment palette, combination guidance, and fallback checks.

Choose effects for the brand and content, not merely to fill empty space. Usually use one dominant treatment and at most one supporting treatment per visual region. Flat space is useful breathing room. Preserve quiet zones behind reading and action areas. Apply a coherent treatment system across sections rather than a different effect everywhere.

Prefer existing assets and lightweight CSS or SVG for simple effects. Use raster assets for photographic or material detail; use available image tools when helpful, but provide a practical fallback when unavailable. Use legitimately available assets and fonts. Keep decorative layers noninteractive and hidden from assistive technology. Never blur, distort, or rasterize essential text to achieve a background effect.

### Mobile onboarding

For onboarding work, also read [Mobile onboarding](references/onboarding.md). Adapt to native or web platform conventions rather than shrinking a desktop landing page into slides.

### Motion and implementation

- Use motion to clarify transitions, focus, or feedback. Respect reduced motion and keep a static equivalent. Introduce continuous effects only when they justify their rendering cost.
- Implement in the existing architecture, reuse components, and keep design values consistent. Avoid adding a dependency for a treatment that existing tools can deliver.
- Keep first-render content and actions available while assets load. Size and compress imagery appropriately; reserve media dimensions, load fonts responsibly, and defer below-the-fold assets. Be cautious with large blur filters, animated noise, and full-screen shaders on mobile.

## Verify and finish

Inspect the rendered result at representative desktop and mobile sizes when the environment permits. Check the full page or complete onboarding path, not only the hero. Verify primary actions, forms, keyboard focus, contrast, overflow, touch targets, reduced motion, and relevant existing project checks. For a native flow, check safe areas and keyboard behavior when the available simulator permits it.

Compare the result with the initial weaknesses and the captured brand baseline. Account for every original visible image at desktop and mobile sizes, and check that palette, theme, fonts, logo, and voice remain recognizable. Restore unauthorized substitutions, removals, or hidden imagery before finishing. Fix concrete regressions and unresolved hierarchy problems before stopping. Do not claim conversion gains or performance improvements without measurements, or visual verification without inspecting the rendered output.

### Recognition and delight review

Before delivering, assess the rendered result against these questions:

- Does it still feel unmistakably like the same brand, with its characteristic colors, imagery, and voice?
- Is the product and primary action easier to understand through concrete improvements in message or hierarchy?
- Is the page more comfortable to read and explore, with deliberate spacing, readable type, and useful interactions?
- Is there a distinctive detail worth remembering that belongs to this brand?
- Do mobile and the rest of the page receive the same care as the hero?

Review the observable improvements from the design brief against the rendered result. For an unmet target or weak answer, name the location, visible symptom, and likely cause before editing. For example: “On the narrow layout, the screenshot labels are unreadable because the desktop composition has been scaled down.” Make a focused correction, render again, and inspect the affected region and any layout it displaced. An assertion that the page “looks better” is not verification.

Stop when the identified issues and relevant regressions are resolved; avoid unrelated aesthetic variants. If a target cannot be verified with available tools, report it as unverified. These are design assessments, not evidence of increased happiness or conversions.

When before screenshots are available, present a comparable before and after using the same viewports and corresponding page regions, with real content and consistent loading states. Explain what improved and what was preserved. If rendering is unavailable, state that limitation rather than implying a visual comparison was performed.

Invite brief owner feedback on what feels better and what feels lost without blocking delivery. When evaluating or refining this skill across real projects, use feedback from several different pages and owners to identify recurring problems; distinguish brand-specific preferences from reusable lessons. Do not contact owners or modify the shared skill without authorization.

Finish with the changes made, the design rationale, and verification performed. State any material limitation, including unavailable browser or device checks. Deliver within the requested scope; do not publish or deploy merely because a redesign is complete.
