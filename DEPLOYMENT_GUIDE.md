# Deployment Guide

## Hostinger static hosting (recommended for this architecture)

This project is a Vite-built single-page React application. It does not need a Node.js runtime in production: Vite compiles the client app to static HTML, JavaScript and CSS in `dist/`.

1. Build with `pnpm install` and `pnpm build` in CI or locally.
2. In Hostinger hPanel, open the target website’s File Manager and upload the **contents** of `dist/` to `public_html/` (or the configured document root).
3. Confirm `index.html`, `assets/`, and `.htaccess` are in the document root. Vite copies `public/.htaccess` into `dist/.htaccess`.
4. Open the home page and a deep link such as `/capabilities` directly. Refresh each deep link to verify Apache rewrites it to `index.html`.

The `.htaccess` rule serves existing files and directories directly and sends remaining routes to the React Router app. If the Hostinger account uses Nginx without Apache overrides, configure its equivalent `try_files $uri $uri/ /index.html;` rule in the site configuration.

## GitHub

Push source and lockfile to the repository’s `main` branch. A static host can build with `pnpm install --frozen-lockfile` and `pnpm build`, then publish `dist/`. GitHub Pages needs a SPA 404 fallback or a routing-aware deployment action; the included `.htaccess` applies only to Apache/Hostinger and is not used by GitHub Pages.

## Node.js hosting plans

A Node.js plan is unnecessary for this static build. Use a Hostinger Node.js application only if a future phase adds server rendering, API routes, or a backend that needs a persistent server. No credentials or runtime environment secrets are required by the current client bundle.

## Routing and assets

`BrowserRouter` uses root-relative routes and Vite’s default `/` base. Deploy at the domain root. If a subdirectory deployment is required, configure Vite’s `base` and Router basename to match it before building. All assets currently used by the replica are served from the local `public/` directory and included in `dist/`; no runtime request to the reference host is required.
