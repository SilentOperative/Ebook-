# EBooksOfficial reconstruction plan

## Implementation approach

Rebuild the public EBooksOfficial experience as a Vite + React single-page application with lightweight client-side routing. The deployed site is the source of truth because the new repository is empty. The restored app covers the observed home, class collections, stream routes, Resource Vault, Tools, What's New, Search, and Help & Fixes pages. The public download destinations are represented as external links, while filtering, view modes, theme switching, navigation, copy-link actions, and search are functional locally.

The app will use a shared utility header and footer, a restrained information-dense card system, remote cover art from the deployed public catalog, and route-aware content arrays so new catalog items can be added without rewriting page layout.

## Design system

Candidate styles: quiet editorial library (0.07); neo-brutalist catalog (0.05); soft academic dashboard (0.04). The selected direction is **quiet editorial library**.

- **Design Movement:** contemporary editorial index with a subtle Swiss grid and an Indian exam-prep resource culture.
- **Core Principles:** scanability first, direct access to resources, transparent metadata, and calm visual density.
- **Color Philosophy:** cloud white and mist blue keep the library light; electric blue marks active actions; mint/yellow chips communicate freshness without noisy decoration.
- **Layout Paradigm:** wide editorial canvas with narrow content measure for hero copy, then full-width shelves and collection trays.
- **Signature Elements:** faint blue grid texture, italic blue emphasis in headlines, and small mono metadata chips around every catalog item.
- **Interaction Philosophy:** searching and filtering should feel immediate; every book card exposes a clear “Download” or “Open” action plus useful guide metadata.
- **Animation:** short lift/fade transitions only; no looping decoration that competes with book discovery.
- **Typography System:** Plus Jakarta Sans for body/UI, Newsreader italic for editorial emphasis, and JetBrains Mono for catalog labels and statistics.
- **Brand Essence:** a fast, curated digital shelf for Class 10–12, JEE, and NEET learners. Personality: calm, useful, transparent.
- **Brand Voice:** direct and lightly witty—“Start where you are.” and “Tools that actually help.”
- **Wordmark & Logo:** compact black EBooksOfficial wordmark with a dark rounded book mark.
- **Signature Brand Color:** electric blue `#2f67ee`.

## Project structure

- `src/main.jsx` — route selection, reusable catalog data, layout, pages, and local interactions.
- `src/styles.css` — grid canvas, responsive breakpoints, typography, cards, shelves, and dark theme.
- `public/manus-routes.json` — all declared public page routes.
- `app.config.ts` — durable project logo metadata.
