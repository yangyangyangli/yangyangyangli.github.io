# SITE_BRIEF.md

## Purpose
Build a faculty-oriented academic website for Yang Li to support Assistant Professor applications in Canada and the United States.

The website is not a generic resume site. It should communicate:
1. A coherent independent research identity.
2. A credible future research program.
3. Strong peer-reviewed outputs.
4. Applied municipal and federal research experience.
5. Methodological depth in GIS, remote sensing, UBEM, LCA, BIM, and data-driven/GeoAI methods.
6. Teaching capacity.
7. International and interdisciplinary collaboration.

## Working research identity
I develop geospatial, building-energy, and life-cycle assessment methods to understand and accelerate urban transitions toward net-zero and low-carbon cities.

## Research program logic
Geospatial urban data
→ 2D/3D city models
→ urban building energy modelling
→ retrofit/electrification/renewable-energy scenarios
→ spatial life-cycle carbon and environmental assessment
→ net-zero urban pathways
→ municipal and policy decision support

## Four research pillars
### 1. Urban Building Energy & Net-Zero Transitions
UBEM, building archetypes, retrofit, electrification, solar energy, district energy, net-zero pathways.

### 2. Geospatial & Data-Driven Urban Modelling
GIS, remote sensing, LiDAR, 2D/3D city models, open data, spatial analysis, GeoAI/data-driven methods.

### 3. Life-Cycle Carbon & Environmental Assessment
Spatial LCA, dynamic LCA, embodied and operational impacts, BIM-LCA, uncertainty, environmental assessment.

### 4. Climate-Responsive Urban Technologies
Green/cool roofs, solar technologies, urban greening, microclimate, passive strategies, climate resilience.

## Website architecture
- Home
- Research
- Projects
- Publications
- Teaching
- Talks
- About
- CV

## Homepage objective
A search-committee member should understand within 20-30 seconds:
- what Yang studies;
- the methods he uses;
- the scale of his work;
- the outputs and applied partners;
- the future research program he is positioned to lead.

## Homepage sections
1. Hero
2. Short research vision
3. Research pillars
4. Featured projects
5. Selected publications
6. Applied research and collaborations
7. Teaching
8. Awards/funding
9. CV/contact

## Flagship projects
### A. GIS-based pathways to urban net-zero energy buildings
Source: Sustainable Cities and Society (2025)
Primary visual story:
open data + archetypes + 3D city model + UBEM → retrofit/electrification/solar pathways.

### B. Spatial GIS-BIM-LCA for urban net-zero buildings
Source: Applied Energy (2025)
Primary visual story:
urban building model → whole-life LCA → spatial impacts → BAU vs net-zero scenarios.

### C. Richmond GIS-based urban building energy assessment
Source: City of Richmond / UBC Sustainability Scholars report (2023)
Primary visual story:
LiDAR/GIS → building-stock model → archetypes → energy/GHG assessment → solar potential.

### D. Geospatial technologies for urban net-zero energy
Source: Journal of Building Engineering (2025)
Primary role:
research-vision / methods / future-directions page rather than a conventional project page.

### E. UBEM + urban-building environmental impact assessment integration
Source: Renewable and Sustainable Energy Reviews (2025)
Primary role:
research-program integration and methods page.

### F. NRC Building LCA Benchmarking
Source currently available: CV entry only.
Treatment:
high-priority experience/project, but do not invent methods, results, figures, or claims until NRC project material is supplied.

## Supporting projects / publications
- GIS for renewable energy in buildings toward net zero (Buildings, 2023)
- Net-zero-energy poultry housing and LCA (2020 thesis; JCP 2021; RSER 2022)
- Spatially resolved pea/lentil LCA and emissions modelling (2022)
- LCA uncertainty review (2020)
- Earlier environmental chemistry research (archive/publications page)

## Academic tone
Use concise, technically precise, evidence-based language.
Avoid:
- exaggerated claims;
- marketing language;
- vague statements such as “world-leading”;
- unsupported claims of impact;
- skill-percentage bars;
- generic stock images.

## Design direction
- al-folio on GitHub Pages.
- Light, clean academic visual system.
- Research maps and diagrams are the main visual language.
- Large project images with generous whitespace.
- One restrained accent color.
- Strong typography.
- Minimal animation.
- Mobile responsive.
- Accessible alt text.
- Keep figure labels readable.

## Content accuracy rules for Claude
- Never invent findings, numbers, grants, affiliations, roles, datasets, software, project results, or publication details.
- If evidence is missing, insert TODO.
- Preserve technical terminology from source publications where possible.
- Do not inflate Yang's role in collaborative projects.
- Do not state NRC project details beyond supplied evidence.
- Keep a distinction between published findings, project reports, and proposed/future research.

## Figure-rights rules
1. For CC BY 4.0 papers, figures can generally be reused/adapted with proper attribution; identify adaptations.
2. Prefer Yang's original exported figure files over screenshots from publisher PDFs.
3. Preserve third-party basemap/data attributions.
4. For CC BY-NC-ND papers, do not adapt/crop/redesign the publisher figure without checking license implications; direct unchanged reuse should be handled cautiously.
5. For all-rights-reserved papers, do not reuse publisher-rendered figures without permission.
6. For the Richmond report, avoid the Getty cover image and Google Earth-derived content on the website. Prefer Yang's original GIS outputs and figures.
7. If a figure includes third-party imagery/icons/maps, preserve or recreate required attribution.

## Suggested al-folio content mapping
- `_pages/about.md` → homepage/about
- `_pages/research.md` → research program
- `_pages/projects.md` → project index
- `_projects/` → individual flagship project pages
- `_bibliography/papers.bib` → publication database
- `_pages/teaching.md` → teaching
- `_pages/talks.md` → presentations
- `assets/img/projects/` → research figures
- `assets/pdf/` → CV and public reports where appropriate
