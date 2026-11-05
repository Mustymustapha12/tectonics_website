# Tectonics Engineering Group website replica

A React, TypeScript, Vite and Tailwind CSS recreation of the publicly accessible Tectonics Engineering Group site. Routing uses React Router; Framer Motion and Lucide React provide transitions and icons.

## Requirements

- Node.js 20.19+ or 22.12+
- pnpm 11 (the checked-in lockfile is `pnpm-lock.yaml`)

## Local setup

```sh
pnpm install
pnpm dev
```

Vite prints the local development URL, usually `http://localhost:5173`.

## Production build

```sh
pnpm build
pnpm preview
```

The production site is a static client-side application in `dist/`.

## Routes

The page inventory is in [PAGE_INVENTORY.md](./PAGE_INVENTORY.md). Visual and route findings are in [REFERENCE_SITE_AUDIT.md](./REFERENCE_SITE_AUDIT.md); reference media paths are listed in [ASSET_INVENTORY.md](./ASSET_INVENTORY.md).

## Deployment

See [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md). This app does not require a Node.js server in production. Hostinger shared hosting can serve the Vite output as static files and use the included Apache rewrite in `public/.htaccess` for React Router refreshes.

## Content and service limitations

Authorized site images are served locally from `public/`; large portfolio and TEGCRETE images use WebP copies to reduce the production payload. The original downloaded PNG files are retained in the ignored `reference-originals/` folder. Contact and TerraBridge application submission are not connected to a backend. TerraBridge form validation runs locally and never sends or stores candidate information; the page tells applicants this limitation. Project and reference cards open item-specific detail modals.

The reference catalogue's 169 entries, descriptions, categories, and pagination are reproduced. Two product photographs referenced by the catalog returned 404 from the reference host; those entries use closely related local product images. The four contact offices and their visible contact details are present; Turkey address data was not independently verified in the captured reference and is left as a contact placeholder. The original TerraBridge video is included locally with a poster, native inline controls and static-file caching. Its source file is approximately 32 MB.
