# Visual QA Report

Audit date: 2026-11-05

## Method

- Compared the live reference and local replica in separate browser tabs at 1440 × 900, using matching URLs and viewport dimensions for the visual captures.
- Captured paired views for the capability index and detail page, projects, references, products, TEGCRETE, About, Contact, TerraBridge, and legal content. The paired screenshots are included in the audit conversation.
- Measured headings and page geometry in the browser, and checked all 18 inventoried routes plus the custom 404 route.
- Checked all 19 URLs at 1440 × 900 and 768 × 900, 390 × 844, and 360 × 800. Checked 1920 × 1080 in the responsive sweep before the last page-specific corrections.

## Corrections made

- Added a light interior-page header treatment with the dark logo to match the reference navigation on content pages.
- Rebuilt the capability index first view as a dark heading and five-column service card layout.
- Replaced the capability detail photo hero with the reference's light editorial heading, return link, three service cards, and image section.
- Reworked the product catalogue first view: heading, search field, summary, category selector, and four-column product cards now align with the reference's measured desktop positions.
- Rebuilt the Projects feature panel as a rounded, inset image panel with the project title, location, and description.
- Rebuilt the References first view as a centered title, pill filters, and three-column reference cards.
- Reworked the Contact hero and enquiry cards to match the reference's centered title, media-enquiry line, and two-card layout.
- Replaced the About photo hero with the reference's company introduction and CEO message card.
- Matched the legal pages' full-width white background, centered reading column, and title position.
- Matched the TEGCRETE black first-view hero and split wordmark styling; adjusted the TerraBridge hero to the reference's dark treatment.
- Fixed the product catalogue's 768px horizontal overflow.

## Route review

| Route | Visual QA result |
| --- | --- |
| `/` | Earlier desktop hero and opening section checks were close; partner, TerraBridge, and impact section heights still differ. |
| `/capabilities` | First view corrected; lower capability descriptions and imagery remain approximate. |
| `/capabilities/geotechnical-civil-infrastructure` | First view now matches the light service-card structure; lower-page composition remains approximate. |
| `/capabilities/digital-laboratory-materials` | First view corrected; the reference contains more gallery/media content below. |
| `/capabilities/environmental-geoscience` | First view corrected; lower-page composition remains approximate. |
| `/capabilities/lab-engineering-ai` | First view corrected; lower-page composition remains approximate. |
| `/capabilities/training-capacity-building` | First view corrected; gallery and lower-page content remain incomplete. |
| `/projects` | Featured project panel corrected; project portfolio content and full-page height still differ. |
| `/references` | First view and card geometry corrected; reference text/data and lower-page content are not exact. |
| `/products` | Catalogue first view and card geometry corrected; some unavailable source product assets use matched substitutes. |
| `/products/tegcrete` | Black hero and wordmark corrected; below-the-fold content remains substantially shorter than the reference. |
| `/initiatives/terrabridge` | Dark hero treatment corrected; the reference has more gallery imagery and a longer page. |
| `/about` | Opening introduction and CEO message card corrected; below-the-fold sections remain incomplete. |
| `/contact` | Hero and two enquiry cards closely match the reference; locations and footer content remain approximate. |
| `/careers` | Route and responsive behavior work; page content and visual structure remain approximate. |
| `/legal/cookies` | Reading-column layout corrected; text content is shorter than the reference. |
| `/legal/privacy` | Reading-column layout corrected; text content is substantially shorter than the reference. |
| `/legal/anti-slavery` | Reading-column layout corrected; text content is shorter than the reference. |
| Custom 404 | Custom not-found route renders and has no horizontal overflow. |

## Verification

- All 19 tested URLs rendered a primary heading at 1440px, 768px, 390px, and 360px.
- No horizontal overflow was detected across those 76 route/viewport checks after fixing the 768px product page.
- No broken images were detected among images that had loaded in the checks.
- `pnpm run build` passed after all page changes (`tsc -b` and Vite production build).
- Catalogue search returned matching product results, category selection returned the category products, and the mobile navigation opened at 390px.
- Static contact/application forms do not transmit or persist submissions; these limitations remain documented in the project README.

## Remaining visual work

This pass materially improves the first viewport for the pages listed above, but it does not establish a pixel-identical full-page match for every route. The largest remaining differences are page length and section content on About, Careers, TEGCRETE, TerraBridge, capability details, and legal pages; project/reference card data and some original media also differ. Footer columns and lower-page sections need another screenshot-by-screenshot pass before the replica can be described as fully faithful.
