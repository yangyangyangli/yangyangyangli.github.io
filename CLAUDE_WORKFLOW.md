# CLAUDE_WORKFLOW.md

## Recommended stack
GitHub Pages + al-folio + Claude Code.

## Phase 0 — Create repository
1. Go to `alshedivat/al-folio`.
2. Choose **Use this template**.
3. Create `<github-username>.github.io`.
4. Clone locally.
5. Create a branch such as `site-build`.

## Phase 1 — Add source package
Add:
- `SITE_BRIEF.md`
- `FIGURE_PLAN.md`
- CV PDF
- publication BibTeX
- selected original research figures
- project notes
- NRC material when available

Suggested folders:
```
assets/
  img/
    projects/
      urban-net-zero/
      spatial-lca/
      richmond-ubem/
      geospatial-review/
      ubem-eia/
      nrc-lca/
  pdf/
_bibliography/
_projects/
_pages/
```

## Phase 2 — First Claude prompt
```text
You are helping me build an academic personal website for Assistant Professor applications in Canada and the United States.

This repository uses the current al-folio template.

FIRST:
1. Read CLAUDE.md and AGENTS.md.
2. Read relevant files under .claude/skills/.
3. Read SITE_BRIEF.md and FIGURE_PLAN.md.
4. Inspect the repository.

Do not modify files yet.

Return:
A. current repository structure;
B. existing al-folio components to reuse;
C. files/pages that should be changed;
D. a phased implementation plan;
E. missing information and TODOs.

Content rules:
- Never invent findings, numbers, roles, grants, affiliations, project results, or methods.
- Use only supplied evidence.
- Preserve academic terminology.
- Use TODO when evidence is missing.
- NRC details must remain limited to supplied project evidence.

Design rules:
- Research maps/figures should be the main visual language.
- Clean, restrained academic design.
- No skill bars, stock photography, excessive gradients, or flashy animation.
- Preserve figure aspect ratios and attribution.
- Add accessible alt text.
- Optimize large images without making labels unreadable.

Wait for approval before implementation.
```

## Phase 3 — Base implementation
Prompt:
```text
Implement Phase 1 only: base al-folio configuration and navigation.

Pages:
Home
Research
Projects
Publications
Teaching
Talks
About
CV

Do not write detailed project pages yet.

Before editing:
- create a git checkpoint;
- preserve template functionality;
- avoid destructive git operations.

After editing:
- run the local build;
- report errors;
- list every modified file;
- explain changes;
- do not push without approval.
```

## Phase 4 — Homepage
Give Claude approved homepage copy and selected images.
Ask it to implement:
- hero;
- research statement;
- 4 pillars;
- 3 featured projects;
- selected publications;
- applied research/collaborations;
- teaching preview;
- CV/contact CTA.

Do not let Claude invent the academic narrative.

## Phase 5 — Project pages
Build one project at a time.

Template:
1. Problem
2. Research question
3. Methods
4. My contribution
5. Key results
6. Significance
7. Related publication/report
8. Code/data/slides where available
9. Figure attribution

Build order:
1. GIS-based urban net-zero pathways
2. Spatial GIS-BIM-LCA
3. Richmond UBEM
4. Geospatial technologies review/research-vision page
5. UBEM + UB-EIA integration
6. NRC LCA benchmarking after source material is supplied

## Phase 6 — Publications
Use `_bibliography/papers.bib`.
Mark a limited number as selected.
Add DOI, PDF, code, data, report, or project links where verified.

## Phase 7 — Teaching / talks / about
Use concise evidence-based content.
Separate:
- teaching experience;
- guest lectures;
- courses Yang can contribute to;
- talks/conferences;
- research visits;
- awards/funding.

## Phase 8 — Visual optimization
For each image:
- use original export when available;
- add alt text;
- add source/attribution;
- use responsive formats;
- preserve legends;
- create smaller thumbnails separately from full-size research figures.

## Phase 9 — QA
Ask Claude to check:
- Jekyll build;
- broken links;
- mobile layout;
- dark mode;
- accessibility;
- figure attribution;
- image loading;
- malformed BibTeX;
- CV link;
- DOI links;
- TODO markers;
- claims unsupported by sources.

## Phase 10 — Human academic review
Before publishing:
- compare each project page with the source paper/report;
- verify numbers;
- verify contribution language;
- verify terminology;
- verify figure licenses;
- verify all collaborations/funding;
- remove unresolved TODOs.

## Phase 11 — Deploy
Push to GitHub only after review.
Enable GitHub Pages / al-folio workflow.
Connect custom domain only after the site is stable.
