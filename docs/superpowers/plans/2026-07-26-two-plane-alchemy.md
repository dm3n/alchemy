# Two-Plane Alchemy Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Revise and release the Alchemy paper so every created reality begins as a
mental form in the mental/astral plane and the embodied human is the alchemical bridge
that materializes it in the physical plane.

**Architecture:** Keep the paper's empirical evidence, four-theorem model, and
ten-section structure. Replace the three-realm ontology at the manuscript,
mathematical, diagrammatic, repository, O-1A, portfolio, itinerary, and memory layers.

**Tech Stack:** LaTeX, BibTeX, TikZ, Poppler, Git, GitHub CLI, Markdown.

## Global Constraints

- Define exactly two planes: mental/astral and physical.
- Treat the conscious and embodied human as the alchemical bridge, not a third plane.
- Use "mental form" for every causal or ontological use of form.
- Preserve grammatical and mathematical uses such as "conditional form."
- Preserve the exact patent and Gateway PDF bytes.
- Add no tables and no unsupported claims of experimental proof.
- Use ASCII hyphens only in newly authored prose.
- Add no AI attribution to commits.

---

### Task 1: Rewrite the Paper Ontology

**Files:**
- Modify: `main.tex`
- Modify: `refs.bib` only if citation changes become necessary

**Interfaces:**
- Consumes: the approved design in
  `docs/superpowers/specs/2026-07-26-two-plane-alchemy-design.md`
- Produces: the complete two-plane LaTeX manuscript

- [ ] **Step 1: Replace the abstract and canonical definition**

State that every created reality begins as a mental form in the mental/astral plane and
that the embodied human carries it into the physical plane.

- [ ] **Step 2: Replace the causal chain**

Use:

```text
mental form -> embodied human bridge -> policy -> action -> physical reality -> feedback
```

- [ ] **Step 3: Replace Sections 2 and 3**

Rename them:

```latex
\section{The Two Planes and the Human Bridge}
\section{The Human Alchemical Bridge}
```

Define only the mental/astral plane and physical plane. Explain embodiment as the
bridge mechanism.

- [ ] **Step 4: Revise the formal model**

Use mental form variable `M_t`:

```latex
P(W_{t+1}\mid M_t,B_t,E_t)
=
\sum_{\pi\in\Pi(B_t,E_t)}
P(W_{t+1}\mid\operatorname{do}(\pi),B_t,E_t)
P(\pi\mid M_t,B_t,E_t).
```

Update the mediation theorem from imaginal states `i_1,i_2` to mental forms
`m_1,m_2`. Preserve the other proof logic.

- [ ] **Step 5: Revise both TikZ diagrams**

Figure 1 must show:

```text
MENTAL/ASTRAL PLANE -> HUMAN ALCHEMICAL BRIDGE -> PHYSICAL PLANE
```

Figure 2 must show:

```text
SOLVE -> MENTAL FORM -> COAGULA
```

- [ ] **Step 6: Propagate mental-form terminology**

Update causal and ontological language in inner alchemy, Gateway, the
counter-alchemical environment, the Great Work, identity, predictions, and conclusion.

- [ ] **Step 7: Run semantic integrity checks**

Run:

```bash
rg -n -i 'three realms|imaginal realm|embodied realm|material realm|embodied plane' main.tex
rg -n '\bform\b' main.tex
rg -n '^\\section' main.tex
```

Expected: no obsolete ontology; every relevant form explicitly means mental form;
exactly ten sections.

- [ ] **Step 8: Commit**

```bash
git add main.tex refs.bib
git commit -m "Clarify the two-plane Alchemy model"
```

### Task 2: Update Repository Documentation

**Files:**
- Modify: `README.md`
- Modify: `docs/research/alchemy-source-map.md`
- Modify: `sources/README.md` only if its paper summary needs the ontology

**Interfaces:**
- Consumes: the final manuscript terminology
- Produces: repository documentation that makes the two-plane model immediately clear

- [ ] **Step 1: Rewrite the README ontology**

Replace "Three realms" with "Two planes and the human bridge." Use the canonical
mental-form chain and update the section list.

- [ ] **Step 2: Rewrite the research source map**

State the two-plane thesis and the role of the embodied human while preserving all
document-type evidence boundaries.

- [ ] **Step 3: Check stale terminology**

Run:

```bash
rg -n -i 'three realms|imaginal realm|embodied realm|material realm|embodied plane' \
  README.md docs/research/alchemy-source-map.md sources/README.md
```

Expected: no matches.

- [ ] **Step 4: Commit**

```bash
git add README.md docs/research/alchemy-source-map.md sources/README.md
git commit -m "Document the two-plane Alchemy thesis"
```

### Task 3: Build and Visually Verify the Paper

**Files:**
- Modify: `main.pdf`
- Generate temporarily: `tmp/pdfs/two-plane-alchemy-*`

**Interfaces:**
- Consumes: `main.tex`, `refs.bib`
- Produces: a warning-free release PDF and visual QA evidence

- [ ] **Step 1: Compile the complete publication**

Run:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

- [ ] **Step 2: Reject build warnings**

Run:

```bash
rg -n 'Warning|Overfull|Underfull|undefined|multiply defined' main.log
```

Expected: no output.

- [ ] **Step 3: Verify text and metrics**

Run `pdfinfo`, `pdftotext`, source/citation counts, section count, and searches for the
two-plane terminology. Record the resulting page, word, citation, theorem, diagram, and
prediction counts in the README.

- [ ] **Step 4: Render and inspect every page**

Render with:

```bash
pdftoppm -png -r 144 main.pdf tmp/pdfs/two-plane-alchemy/page
```

Inspect contact sheets and full-resolution pages containing both diagrams. Reject
clipping, awkward wraps, sparse pages, overlaps, and broken references.

- [ ] **Step 5: Commit**

```bash
git add main.pdf README.md
git commit -m "Publish the two-plane Alchemy edition"
```

### Task 4: Publish the Paper and Replace O-1A Paper #4

**Files:**
- Update: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - Alchemy/Alchemy.pdf`
- Update: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - Alchemy/main.tex`
- Update: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - Alchemy/refs.bib`
- Update: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - Alchemy/README.md`
- Update: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - Alchemy/sources/README.md`

**Interfaces:**
- Consumes: the clean paper repository release
- Produces: a byte-matched O-1A Paper #4 bundle

- [ ] **Step 1: Push the Alchemy repository**

Run:

```bash
git push origin main
```

- [ ] **Step 2: Copy the current release into O-1A**

Copy `main.pdf` as `Alchemy.pdf` and copy the current source, bibliography, README, and
source README. Preserve both source PDFs.

- [ ] **Step 3: Verify O-1A byte identity**

Run `cmp` for the PDF, LaTeX source, bibliography, README, source README, patent, and
Gateway memorandum. Every comparison must exit 0.

### Task 5: Update Portfolio and Itinerary

**Files:**
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/README.md`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/docs/08-o1a-evidence-map.md`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/docs/11-research-alchemy.md`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/Daniel_Edgar_Technical_Portfolio.tex`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/Daniel_Edgar_Technical_Portfolio.pdf`
- Rebuild: `/Users/dm3n/Desktop/O-1A/Itinerary + portfolio.pdf`

**Interfaces:**
- Consumes: the final paper terminology and metrics
- Produces: consistent public portfolio and O-1A itinerary

- [ ] **Step 1: Replace the three-realm summary**

Every portfolio surface must state two planes and identify the human as the alchemical
bridge. Use the final release metrics.

- [ ] **Step 2: Rebuild the portfolio and itinerary**

Run:

```bash
./build-itinerary.sh
```

Expected: technical portfolio compiles and the combined itinerary is rebuilt.

- [ ] **Step 3: Render and inspect the itinerary**

Render all pages with `pdftoppm`, inspect contact sheets, and inspect the page containing
the Alchemy summary at full resolution.

- [ ] **Step 4: Commit and push**

```bash
git add README.md docs/08-o1a-evidence-map.md docs/11-research-alchemy.md \
  Daniel_Edgar_Technical_Portfolio.tex Daniel_Edgar_Technical_Portfolio.pdf
git commit -m "Update the portfolio for two-plane Alchemy"
git push origin main
```

### Task 6: Update Brain and Verify the Release

**Files:**
- Modify: Brain `Memory/project_alchemy_paper4.md`
- Modify: Brain `Memory/project_o1a_ai_portfolio_repo.md`
- Modify: Brain `Wiki/Concepts/Alchemy as Materialization.md`
- Modify: Brain `Wiki/log.md`

**Interfaces:**
- Consumes: final commit IDs, hashes, and metrics
- Produces: persistent continuity and a complete release audit

- [ ] **Step 1: Update persistent records**

Record the two-plane ontology, human-bridge thesis, final hashes, commit IDs, and
artifact page counts.

- [ ] **Step 2: Run the release audit**

Verify:

- both repositories are clean and synchronized with `origin/main`;
- the paper compiles from a fresh temporary directory with a clean log;
- exactly two planes are defined and obsolete ontology is absent;
- source hashes match their preserved values;
- O-1A Paper #4 byte-matches the paper release;
- the portfolio and itinerary contain the revised thesis and no three-realm language;
- Brain records contain the final commit IDs and hashes.

- [ ] **Step 3: Require an explicit pass marker**

The audit must exit 0 and print:

```text
ALL_TWO_PLANE_RELEASE_CHECKS_PASSED
```
