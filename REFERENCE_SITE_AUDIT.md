# Reference Site Audit

**Reference:** https://tectonicsgroup.co.uk/  
**Audit date:** 5 November 2026  
**Scope:** Public pages reachable from homepage navigation, body links, and footer. Inspection included narrow and desktop browser captures, rendered text, image paths, styles, and interaction checks. Some media lazy-loads, so captures were allowed to settle before measurements.

## Discovered pages

| Route | Page | Findings |
|---|---|---|
| `/` | Home | Hero promotion for TEGCRETE; capability selector; project CTA; three featured capability cards; partner logos; TerraBridge feature; impact list; shared footer. |
| `/capabilities` | Capabilities | Hero “Engineering the Future of West Africa”; five capability summaries followed by detailed sections and CTA. |
| `/capabilities/geotechnical-civil-infrastructure` | Geotechnical & Civil Infrastructure | Back link, title/intro, site investigations, foundation design, pavement analysis, photo, project CTA. |
| `/capabilities/digital-laboratory-materials` | Digital Laboratory & Materials Testing | Testing services, standards/data integrity, equipment distributor section, product images, facility gallery, quote CTA. |
| `/capabilities/environmental-geoscience` | Environmental & Geoscience | Impact assessments, geoscience surveys, compliance audits, sustainability CTA. |
| `/capabilities/lab-engineering-ai` | Lab Engineering & AI Solutions | Lab design, AI integration, supply/commissioning, distributor and future-ready laboratory content. |
| `/capabilities/training-capacity-building` | Training & Capacity Building | Workshops, standards curriculum, TerraBridge program, video, training gallery. |
| `/projects` | Projects | Featured Kabusa project, portfolio of 22 projects, search input, category select/filter and project cards. |
| `/references` | Local & Regional References | Track-record intro, category filters, 22 reference cards with category/client/location/details. |
| `/products` | Products & Materials | Catalogue with 169 items, category filters and product/category descriptions and images. |
| `/products/tegcrete` | TEG CRETE™ | Product hero, science/benefits, technical specifications, performance, use cases, product CTA. |
| `/initiatives/terrabridge` | TerraBridge Initiative | Application hero, program overview, metrics, gallery/video, benefits, requirements and application form. |
| `/about` | About Us | Company intro, CEO message, TEGEC initiative, vision/foundation/outcomes/objectives, values, exploration links. |
| `/contact` | Contact | Contact intro and enquiry types, four location cards (Nigeria, Ghana, UK, Turkey), shared CTA/footer. |
| `/careers` | Careers | Careers hero, employer proposition, values/culture sections and “no open positions” notice. |
| `/legal/cookies` | Cookie Policy | Policy text, effective date and numbered sections. |
| `/legal/privacy` | Privacy Policy | Privacy text, data categories, uses, retention and rights. |
| `/legal/anti-slavery` | Modern Slavery Statement | Statement, supply-chain and due-diligence sections, training and values. |

The footer “Impact” link resolves to `/capabilities/training-capacity-building`; it is an alias in the current public navigation, not a distinct impact page. Project/reference cards expose detail affordances, but no separate project-detail routes were identified in the rendered links. The TerraBridge form and contact/location controls need interaction-level verification before their backend behavior can be replicated.

## Navigation structure

- Fixed header: home/logo link; desktop links for Capabilities, Projects, Products, About, Contact, TEGCRETE™ NEW and TerraBridge; mobile menu button.
- Homepage “Let’s Build” list links to TEGCRETE and the five capability detail routes.
- Homepage featured cards link to Geotechnical, Digital Laboratory, and Lab Engineering pages.
- Footer has Services, Discover, Company, and Social/legal columns. Social destinations: LinkedIn, X, Facebook, Instagram.
- Internal CTA links include contact, products, capabilities, projects, references and TerraBridge.

## Homepage, section by section

1. **Combined rotating hero and “Let’s Build” selector:** full viewport-height, two-column section under a fixed transparent/gradient header. A darkened full-bleed background image and capability/promotion message occupy the left half; the right half has a vertical rule, “Let’s Build” heading and six links (TEGCRETE™ plus five capabilities). Selecting a capability changes the active hero message/background and Learn More destination; the hero also advances automatically. At 1440 × 900 the hero is 900 px high, the inner container begins around x=104, and the split is around x=720. TEGCRETE uses `/assets/images/tegcrete/hero.png`.
2. **Drive your project forward:** warm off-white section beginning at y=900 in the 1440 × 900 capture; light-weight headline, short explanatory copy, outlined CTA, then three image-led service cards.
3. **Partner ecosystem:** pale grey background, heading and explanatory paragraph, horizontally arranged partner/manufacturer logos.
4. **TerraBridge feature:** black full-width section, large white heading, explanatory copy, gold CTA and image/video media.
5. **Global impact:** charcoal section with headline, intro and six impact statements (innovation, foresighting, investment, STEM workforce, partnerships, industrial policy).
6. **Footer CTA and footer:** dark background; “Let’s build together” heading, gold button, link groups, social icons, legal links and copyright.

### Desktop screenshot comparison at 1440 × 900

The local and reference homepage captures were compared in the browser at the same 1440 × 900 viewport. Both use a 900 px hero; the second section begins at y=900 and is 828 px high in both. The hero text and selector now use matching line wraps and near-matching positions. Partner section heights are 544 px in the reference and 506 px locally; TerraBridge is 590 px in the reference and 630 px locally. The impact section begins within 4 px of the reference and is 432 px in both after layout tuning. At 1920 × 1080 both hero sections measure 1080 px, with the local hero using the reference's wider inner-container alignment. Matching screenshot pairs were also captured at 768, 390 and 360 px. Header button spacing, exact logo/nav sizing and some lower section media/copy remain visible differences for further visual passes.

## Other page patterns

- Most pages reuse the same fixed header and footer CTA/footer.
- Capability detail pages use back-to-capabilities navigation, prominent title/intro, alternating service content/media, then contact CTA.
- Projects uses featured-project hero plus searchable/filterable grid; References uses category-filtered portfolio cards.
- Products uses a large catalogue and category navigation; TEGCRETE has a bespoke product landing page.
- Contact uses a hero image and location cards; TerraBridge has application-oriented content and form.
- Legal pages are long-form text pages with numbered headings and shared footer.

## Design specifications

- **Typography:** browser-computed stack is Tailwind/system sans-serif (`ui-sans-serif, system-ui, ...`); no custom web font was observed. Headlines are generally light-weight, with bold used for selected feature headings. Body text is regular.
- **Palette sampled from page styles:** primary charcoal `#1A1A1A`; gold `#E3BC42`; warm paper `#FDFBF7`; pale grey `#F5F5F5`; overall document background sample `rgb(242, 242, 242)`; white `#FFFFFF`.
- **Header:** fixed, 80 px high, black-to-transparent vertical gradient; white logo and mobile hamburger. Desktop navigation is hidden below Tailwind `lg` breakpoint; menu button is shown.
- **Buttons:** compact uppercase/tracked treatment in places; outlined dark CTA on light backgrounds; gold fill on dark backgrounds; hero uses translucent white glass-like fill with blur and a pill radius.
- **Homepage sampled at 628 px width:** hero `100vh` (718 px in inspected browser), next section begins at y=718; “Drive” section uses `py-24`; partner area sampled at y≈2501; TerraBridge area black with `py-32`; impact section charcoal with `py-24`; footer starts after impact. These are browser measurements at one mobile-sized viewport, not universal breakpoints.
- **Content width/layout:** page-wide sections; inner content padded 24 px at the inspected narrow viewport. Three homepage service cards stack at narrow width. Logo row and galleries may overflow/scroll or reflow; verify behavior at target sizes.
- **Motion:** hero background/copy rotate among TEGCRETE and five capability messages; selecting a right-side item updates the active slide. Button and selected-link styles transition. The reference itself is not built with Framer Motion.

## Media inventory summary

The site uses original logo and photography/product imagery. Homepage observed assets include `/assets/logos/logotecbg_white.png`, `/assets/images/tegcrete/hero.png`, `/images/projects/dawaki-soil.png`, `/assets/hero/lab1.jpg`, `/assets/images/upgrade.webp`, partner logos under `/assets/logos/`, and TerraBridge imagery under `/assets/images/`. Page-specific assets are catalogued in `ASSET_INVENTORY.md`. Images are frequently served through Next.js optimized image URLs (`/_next/image?...`).

## Interactive functionality to reproduce

- Desktop navigation and mobile menu; active/hover states and dropdown behavior where present.
- Capability selection/links, hero Learn More, CTA buttons, footer links and social links.
- Projects search and category filter; References category controls; Products categories/search or filter.
- TerraBridge gallery/video and application form.
- Contact location “View Details” controls and enquiry links.
- Any image/gallery modal and project “View Details” behavior discovered during implementation verification.

The TerraBridge page has a required application form with full name, email, current position, motivation textarea, and PDF CV/portfolio upload (maximum 500 KB). It includes hidden subject/recipient/message fields. The form was inspected but not submitted. The replica validates required fields and PDF size locally and explains that it does not send or store submitted details. Contact enquiry links lead to contact/email pathways; no new backend is configured.

## Responsive observations

- At 628 px viewport width, header is 80 px with a 24 × 24 hamburger at the right; desktop nav is hidden. Logo remains at left.
- At 768 px, the reference retains the side-by-side hero but uses the hamburger header; below the tablet breakpoint, its capability selector moves beneath the hero message. The reference document measured 784 px wide at a 768 px viewport (16 px overflow); the local page stays within the viewport.
- Homepage hero occupies the viewport height and capability navigation appears beneath it. The main “Drive” heading is 36 px; partner heading is 30 px; TerraBridge heading is 48 px; impact heading is 36 px at this width.
- Narrow layout uses 24 px horizontal content padding and stacked content. Three homepage service cards stack at narrow width. The product catalogue compresses its category filter into a select and pagination into compact controls on mobile.
- Local responsive checks have now been run at 1920, 1440, 768, 390 and 360 px for homepage and catalogue; no horizontal overflow or broken image elements were observed in those captures. Homepage screenshot pairs were captured at all five requested widths. Detailed per-section side-by-side comparison remains ongoing.

## Audit limitations and follow-up

All 18 linked internal routes above were opened in the browser and their headings, copy, and image sources inspected. The audit did not submit forms, which would transmit data. The replica implements all 18 routes and all 169 catalog entries; two catalog image URLs were unavailable and use matched local replacements. Turkey address information remains unverified. The local production build succeeds; local homepage and catalogue were checked at the five requested widths for overflow and missing images. All routes and the custom 404 were opened locally at 360 px; product search/category/pagination/detail interactions and navigation have been exercised. Homepage screenshot comparisons cover each target viewport; per-section comparison of every other route is not complete, so complete visual fidelity is not claimed.
