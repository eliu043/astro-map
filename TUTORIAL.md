# Interactive mapping tutorial progress

Based on https://designpractices.org/tutorials/09-interactive-mapping-part-2/ using the course Astro template.

## Completed locally

- Installed the template and dependencies.
- Set the site name to Astro Map.
- Configured GitHub Pages for `https://eliu043.github.io/astro-map/`.
- Added the supplied `map_toner.json` as `public/style.json` and connected it in `src/maps/full-page.yaml`.
- Replaced the style's placeholder MapTiler tile and font endpoints with OpenFreeMap endpoints. Replaced Nunito label fonts with available Noto Sans fonts. The original file in Downloads is unchanged.
- Kept the starting view over Central Park to show the template's sample data. The San Francisco view saved in the style is overridden by the YAML map configuration.
- Verified the map renders, the bike-lane toggle works, and clicking a squirrel opens its popup.
- Updated the compatible maplibre-yaml core dependency; npm audit reported no vulnerabilities afterward.

## Run locally

Use Node 24 (`.node-version` records this requirement). With fnm:

```sh
fnm install 24
fnm use 24
npm ci
npm run dev
```

Open http://localhost:4321/astro-map/full_page_map.

For this setup session, a temporary Node 24 runtime is also available:

```sh
PATH=/tmp/astro-map-node-runtime/node_modules/.bin:$PATH npm run dev
```

`npm run build` checks Astro and all map/story YAML files, then produces `dist/`.

## Still to finish

1. Sign in to GitHub and create the public `eliu043/astro-map` repository.
2. Push this project to its `main` branch.
3. In repository Settings → Pages, choose GitHub Actions as the source.
4. Verify the Deploy to GitHub Pages workflow and the published map at `https://eliu043.github.io/astro-map/full_page_map`.

The GitHub address above is configured but is not yet a verified live site.
