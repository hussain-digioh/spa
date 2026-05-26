# Digioh SPA QA

A minimal Vue 3 + Vite SPA for QA testing Digioh campaigns with display conditions.

## Routes

| Route | Purpose |
|---|---|
| `/` | Home — trigger campaigns with display condition set to the home URL |
| `/about` | About — trigger campaigns with display condition set to `/about` |

## Setup

```bash
npm install
npm run dev
```

The dev server runs at `http://localhost:5173`.

## How Digioh is wired up

**Script tag** (`index.html`):
The Digioh async script is loaded once in `index.html`. It persists across all SPA route changes.

**Universal merge tag** (`src/components/DigiohWidget.vue`):
A reusable component that renders the `digioh_universal_smart_tag` div. It is placed in `App.vue` directly below the nav bar, so it appears as the hero section on every page. Digioh's display conditions control which campaign renders inside it per route.

To use the widget on a specific view only, remove it from `App.vue` and drop `<DigiohWidget />` directly in that view.

## Campaign display condition tips

- **Home campaign**: set URL contains `/` or exact match `http://localhost:5173/`
- **About campaign**: set URL contains `/about`

## Project structure

```
src/
  components/
    DigiohWidget.vue   ← universal merge tag, reusable
  views/
    HomeView.vue       ← / route content
    AboutView.vue      ← /about route content
  router/index.js      ← Vue Router config (history mode)
  App.vue              ← nav + DigiohWidget + RouterView
  main.js
  style.css            ← global CSS variables and base styles
index.html             ← Digioh script tag lives here
.env                   ← VITE_APP_TITLE
```

## Environment

| Variable | Default |
|---|---|
| `VITE_APP_TITLE` | `Digioh SPA QA` |
