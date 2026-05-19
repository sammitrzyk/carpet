---
name: carpet-guys-design
description: Use this skill to generate well-branded interfaces and assets for Carpet Guys, a residential + commercial carpet cleaning company in Central Pennsylvania, either for production or throwaway prototypes/mocks. Contains essential design guidelines, colors, type, fonts, real photography, and a website UI kit.
user-invocable: true
---

Read the `README.md` file within this skill, and explore the other available files (`colors_and_type.css`, `assets/`, `ui_kits/website/`).

Core rules to internalize before you design:

1. **Two parallel journeys.** Residential = flat per-area pricing + Book Online. Commercial = variable + Request a Quote. Every page should make this distinction obvious. The tagline is *Flat prices for homes. Clear quotes for businesses.*
2. **Voice is local, plain-spoken, you-not-we.** No marketing fluff. No "passionate about delivering." No emoji. No exclamation marks in body.
3. **Type is loud.** Anton display, ALL CAPS for H1/H2. Archivo for sub-heads. Manrope for body.
4. **Color discipline.** Cream `#F7F5EE` for residential, ink `#0E1110` for commercial/contrast, green `#7ED321` only for CTAs and brand. No gradients, no glassmorphism, no neon.
5. **Real photos only.** Every image must be a real Carpet Guys asset from `assets/`. Never invent stock photography. If you don't have an image, leave a placeholder and flag it.
6. **No icon decoration.** Lucide at 1.5px stroke, used to label things only. The mascot character is reserved for footer/favicon/404.

If creating visual artifacts (slides, mocks, throwaway prototypes, single landing pages, etc), copy assets out of `assets/` and create static HTML files for the user to view. Always start by importing `colors_and_type.css` and using the tokens — don't redefine colors or type inline.

If working on production code, copy assets and read `README.md` end-to-end to become an expert in designing with this brand.

If the user invokes this skill without any other guidance, ask them what they want to build or design (homepage section? specific service page? print flyer? slide deck?), ask 4–8 questions about audience, scope, residential-vs-commercial framing, and CTA, and act as an expert designer who outputs HTML artifacts _or_ production code, depending on the need.
