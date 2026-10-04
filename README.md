# Shenyi Zhang's portfolio

Personal engineering portfolio at https://shain.info, built with Parcel, HTML and Sass. The visual foundation comes from [Simplefolio](https://github.com/cobiwave/simplefolio); the original license is retained.

## Run locally

Use Node.js 22, matching `.nvmrc` and `netlify.toml`.

```sh
nvm use
npm ci
npm start
```

## Edit content

- `src/index.html`: introduction, current work, earlier projects and contact links.
- `src/styles.scss`: typography, colors, layout and responsive behavior.
- `src/assets/profile.jpg`: existing portrait.
- `src/index.js`: optional enhancement for the footer year; content and navigation work without JavaScript.

Keep work descriptions public-facing. Do not add internal project identifiers, credentials, raw review documents, unverified ownership, or projected results presented as achieved outcomes. Do not infer employment dates.

The old resume asset is retained in source history but is not linked or included in the current build. Publish a replacement download only after preparing an updated resume.

## Build and preview production output

```sh
npm run build
python3 -m http.server 4173 --directory dist
```

Open http://localhost:4173. The deployable site is the `dist/` directory. It contains only the referenced public assets, with no source maps or raw experience notes. Relative asset URLs also support the existing GitHub Pages project path.

## Deployment

The custom domain is served by Netlify. `netlify.toml` declares `npm run build` and the `dist` publish directory. If the existing Netlify site is connected to this repository, publishing `main` can trigger a build; confirm the actual site integration in Netlify rather than assuming it is connected. For a manual deployment, upload only the contents of `dist` to the existing site, then verify https://shain.info.

The existing GitHub Pages workflow is also retained and updated. It builds on pull requests, and publishes the `gh-pages` branch on a push to `main` or a manual run. This does not prove the custom Netlify domain has updated.

Before publishing, check the production build at desktop and mobile widths, keyboard navigation, links, and image loading. Verify the public domain after publication. Use an earlier successful Netlify deploy to roll back if needed; source changes can be reverted with a new commit.
