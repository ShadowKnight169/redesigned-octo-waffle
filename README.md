# CDL Offline Quiz / Test CDL sin conexión

This is the existing CDL practice website with an English / Spanish (Spain) language switch.

## What changed

- Added **EN / ES** buttons at the top of the page.
- Translated the interface and every question and answer choice in all six banks (488 questions total) to **es-ES**.
- Saved the chosen language in the visitor's browser (localStorage).
- Kept the existing English originals, correct-answer indexes, test lengths and pass thresholds.
- Kept the question order and the currently selected answer unchanged when switching languages.
- Added the Spanish translation file to the offline service-worker cache.
- Adjusted the Spanish controls for narrow mobile screens.

## Publishing on GitHub Pages

Replace the existing files in the root of your GitHub Pages publishing directory with the contents of **this folder** (not an additional nested folder):

- `index.html`
- `translations-es.js` (required for the Spanish text)
- `manifest.json`
- `sw.js`
- `assets/` (keep the original images)

Commit the changes. After the site publishes, refresh the page. If you installed the web app previously, restart it or reload again so the new service worker can activate.

## Editing the translations

The Spanish text for the questions and choices is in `translations-es.js`. The source lines are also in `locale/*.txt` and follow the exact English question order in each bank, with `|` separating the question and its answer choices. Don't change the order of choices unless you also update the matching answer indexes in the English data.

**Important:** The questions concern U.S. commercial driver's license requirements. Measurements such as miles, feet, pounds, and psi are deliberately unchanged, as are the answers. These study translations are not official or verified DMV examination translations.
