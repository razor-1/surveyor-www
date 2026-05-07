# Codesift Marketing Site

This is the marketing website for **Codesift** — an AI platform for coding (categorizing) open-ended survey responses.

## Key Value Proposition

Codesift charges based on **data processed** (tokens/characters), NOT per response. This makes it dramatically cheaper than competitors who charge ~$0.02/response, especially for high-volume or short-response datasets.

## Tech Stack

- **Astro v6** (static site generation, `output: 'static'`)
- **Package manager**: `bun` (always use `bun`, never `npm`)
- **No frameworks**: Pure Astro components, no React/Vue/etc.
- **Styling**: Scoped component styles + `src/styles/global.css` (no Tailwind, no CSS frameworks)
- **Fonts**: Syne (display, weights 700/800) + Plus Jakarta Sans (body, weights 400/500) via Google Fonts

## Design System

- **Color palette** (defined in `src/styles/global.css`):
  - Dark ink background: `#09090F` (`--color-background`)
  - Warm amber accent: `#E8922A` (`--color-accent`)
  - Text colors: `--color-text`, `--color-text-muted`
- **Visual style**: Dark theme with dot grid texture on `body::before`
- **Hero feature**: Animated demo panel showing survey responses being tagged in real-time

## File Structure

```
src/
├── layouts/
│   └── Layout.astro          # Base HTML shell, imports global.css + fonts
├── pages/
│   └── index.astro           # Homepage, composes all components
├── components/               # All page sections
│   ├── Nav.astro
│   ├── Hero.astro
│   ├── HowItWorks.astro
│   ├── Features.astro
│   ├── PricingComparison.astro
│   ├── Testimonials.astro
│   ├── CallToAction.astro
│   └── Footer.astro
└── styles/
    └── global.css            # CSS variables, resets, utilities
public/
└── favicon.svg               # Amber sieve/filter icon
```

## Development Commands

```bash
bun run dev      # Start dev server
bun run build    # Build static site to dist/
```

## Git Practices

**When creating new files or components, always stage them in git immediately after creation.** This helps track all changes in the working tree.

```bash
git add <new-file>
```

## Development Guidelines

1. **Always use `bun`** for package management and scripts, never `npm`
2. **Keep components pure**: No client-side JavaScript frameworks — use Astro's component model
3. **Use CSS variables**: Reference colors and spacing from `global.css` rather than hardcoding values
4. **Component styles**: Keep styles scoped within `<style>` tags in each `.astro` component
5. **Static output**: This site generates static HTML — no SSR or dynamic routes needed
6. **Maintain design consistency**: Follow the dark ink + amber accent color scheme throughout

## Competitors Context

- **BTInsights**: Purple/professional aesthetic, "AI Copilot for Interview and Survey Analysis"
- **SurveyCat**: Casual tone, per-response pricing ($0.02/response), "Turn messy open-text into actionable data"

Codesift differentiates by emphasizing **transparent, usage-based pricing** and being dramatically more cost-effective for bulk analysis.
