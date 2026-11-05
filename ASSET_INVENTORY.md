# Asset Inventory

Assets below were identified from rendered image elements and page markup on the reference site. Original source files are hosted at `https://tectonicsgroup.co.uk`; URLs are listed for implementation acquisition and attribution. Next.js may expose transformed versions through `/_next/image`.

## Brand and shared media

| Asset | Reference path | Use |
|---|---|---|
| Main logo | `/assets/logos/logotecbg.png` | Header and shared brand. |
| White logo | `/assets/logos/logotecbg_white.png` | Homepage hero/header variant. |
| Controls logo | `/assets/logos/Controls.png` | Partner logo. |
| Global logo | `/assets/logos/global-logo.webp` | Partner logo. |
| W+W logo | `/assets/logos/w-w-logo.webp` | Partner logo. |
| MC mark | `/assets/logos/mc.jpg` | Partner logo. |
| IMM2 mark | `/assets/logos/imm2.jpeg` | Partner logo; natural size did not load in initial observation. |
| Homepage hero | `/assets/images/tegcrete/hero.png` | TEGCRETE promotion/hero. |
| Homepage project image | `/images/projects/dawaki-soil.png` | Geotechnical feature card. |
| Homepage laboratory image | `/assets/hero/lab1.jpg` | Materials testing feature card. |
| Homepage lab equipment image | `/assets/images/upgrade.webp` | Laboratory solutions feature card. |
| TerraBridge feature | `/assets/images/labterra01.jpeg` | Homepage initiative feature (natural dimensions unavailable on first load). |

## Page-specific media observed

- Capabilities index: `/assets/hero/capabilities-new.png`, `/assets/images/geotech-hero-african.png`, `/assets/hero/lab1.jpg`, `/assets/hero/home.jpg`, `/assets/hero/lab14.jpg`, `/assets/hero/terrabridge-hero.jpeg`.
- Projects: `/images/projects/kabusa-district.png`, `/images/projects/abuja-north-west.png`, `/images/projects/takum-bissaula.png`, `/images/projects/zaria-panbegwa.png`, `/images/projects/wudil-kwanar.png`, `/images/projects/kwoi-erosion.png` plus further portfolio imagery.
- About: `/assets/images/Aisha.webp`.
- Contact: `/assets/backgrounds/contact-hero.jpg`.
- TEGCRETE: `/assets/images/tegcrete/hero.png`, `/assets/images/tegcrete/tegcrete-infographic.png`, `/assets/images/tegcrete/how-it-works.png`, `/assets/images/tegcrete/application.png`.
- TerraBridge: `/assets/images/Terra1.jpeg`, `/assets/images/tb.jpeg`, `/assets/images/tb1.jpeg`, `/assets/images/tb2.jpeg`, `/assets/images/tb3.jpeg`, `/assets/images/tb4.webp` through `/assets/images/tb10.webp` (recovered WebP renditions).
- TerraBridge original video: `/assets/videos/Terrabridge1.mp4` (approximately 32 MB). Used for the muted looping hero background and controlled inline playback; `/assets/images/tb.jpeg` is the poster/fallback image.
- Geotechnical detail: `/assets/hero/geotechnical-civil.png`.
- Digital laboratory: `/assets/hero/ampt.webp`, `/assets/hero/labtour2.jpeg`, `/assets/hero/lab9.jpg`, `/assets/hero/lab14.jpg`; gallery imagery under `/assets/images/lab1.jpg`, `/assets/images/lab2-1.jpg`, `/assets/images/lab3-1.jpg` and further lab assets.
- Training page: `/images/training/MD_arise.jpeg`, `/images/training/Terra1.jpeg`, `/images/training/Terra2.jpeg`, `/images/training/Terrabridge.jpeg`, `/images/training/labterra01.jpeg`, `/images/training/labtour1.jpeg`, `/images/training/labtour2.jpeg` and additional evidence images.
- Products catalogue: category images include `/assets/images/assessment%20of%20fines.webp`, `/assets/images/particleshape.webp`, `/assets/images/samplesplitters.webp`, `/assets/images/mechanical.webp`, `/assets/images/density.webp`, `/assets/images/frag.webp`, `/assets/images/moist.webp` and additional product imagery.

## Acquisition notes

The listed assets are originals available from the public reference host, subject to the project authorization stated by the user. Preserve aspect ratio and crop behavior from reference screenshots. Optimize local copies for delivery while keeping sufficient resolution for full-bleed desktop imagery. Confirm any inaccessible or missing files against the rendered page before substituting; log substitutes here.

## Local replica files

The reference images used by the implementation have been copied into `public/` and served locally. Portfolio project images, three TEGCRETE images, and product-card images are stored locally. The catalog's two image paths `/assets/images/chemtest.webp` and `/assets/images/mold.webp` returned 404 from the reference host; their cards use related local product photographs instead. Large original project/TEGCRETE PNG-named files are kept under the ignored `reference-originals/` folder and are not copied into the production build. Two Unsplash lab images shown in the reference are represented with local Tectonics lab photographs instead of a third-party image dependency.


## Phase 2 asset recovery notes

The original TerraBridge MP4 and seven missing gallery images were retrieved from the reference site. A few reference entries use suitable local portfolio/laboratory photos because their own per-project photography was not exposed in the source page. The original video is large (about 32 MB); both video elements use `preload="none"` and the hero is muted/inline for browser autoplay compatibility.
