# Page Inventory

Public internal routes discovered from the reference navigation and footer:

| Route | Page type | Main content / behavior |
|---|---|---|
| `/` | Landing | TEGCRETE hero, capability chooser, service cards, partner logos, TerraBridge feature, impact, footer. |
| `/capabilities` | Index | Five capability summaries and detailed sections. |
| `/capabilities/geotechnical-civil-infrastructure` | Capability | Investigations, foundations, pavement, contact CTA. |
| `/capabilities/digital-laboratory-materials` | Capability | Materials testing, standards, equipment, gallery, quote CTA. |
| `/capabilities/environmental-geoscience` | Capability | Assessments, surveys, compliance and contact. |
| `/capabilities/lab-engineering-ai` | Capability | Lab design, AI, supply and commissioning. |
| `/capabilities/training-capacity-building` | Capability | Training, standards, TerraBridge, video and gallery. |
| `/projects` | Portfolio | Featured project, 22 cards, search/category controls. |
| `/references` | Portfolio | Regional references, category filters and cards. |
| `/products` | Catalogue | All 169 product entries, exact descriptions/categories, search, category filters, 24-item pagination, and detail modals. |
| `/products/tegcrete` | Product | TEGCRETE science, specs, benefits and enquiry CTA. |
| `/initiatives/terrabridge` | Initiative | Program information, gallery/video, requirements and application form. |
| `/about` | Company | About, CEO message, TEGEC, vision, outcomes, strategy and values. |
| `/contact` | Contact | Enquiries and four office location cards. |
| `/careers` | Company | Careers overview, culture and current vacancy status. |
| `/legal/cookies` | Legal | Cookie policy. |
| `/legal/privacy` | Legal | Privacy policy. |
| `/legal/anti-slavery` | Legal | Modern Slavery Statement. |

“Impact” in the footer points to `/capabilities/training-capacity-building`. Portfolio cards and product catalog entries may have detail affordances; distinct item routes were not discovered in this route inventory.

## Implementation coverage

All 18 routes above have a React route, including a custom 404 fallback. The product catalog reproduces all 169 entries and paginates 24 per page. Page-specific legal text is a concise reconstruction rather than a verified verbatim transcription.
