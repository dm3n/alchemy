# From Vision to Reality Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the first edition with a concise, professional paper that formally explains how visualization becomes physical change through embodied policy, action, and feedback, then release it across GitHub and the O-1A portfolio.

**Architecture:** Rewrite `main.tex` around one three-layer causal chain and three compact formal results. Preserve the existing bibliography and primary-document archive, update all release copy from measured final statistics, then rebuild and visually verify the paper and merged O-1A itinerary.

**Tech Stack:** LaTeX, BibTeX, TikZ, Poppler, Git, GitHub CLI, shell release scripts.

## Global Constraints

- Title: `From Vision to Reality: A Formal Theory of Embodied Manifestation`.
- Target 5,500 to 6,500 extracted words and approximately 16 to 18 pages.
- Use three formal results, two diagrams, and one compact claim-audit table.
- Treat the patent and Gateway memorandum as primary documentary evidence, not conclusive experimental validation.
- Preserve the exact source PDFs and their hashes.
- Use ASCII hyphens only; no em dashes or LaTeX triple hyphens.
- Keep Daniel as the sole author and add no AI attribution.
- Work directly in the clean canonical repositories because Daniel explicitly requested an end-to-end rewrite and release.

---

### Task 1: Rewrite the paper and repository narrative

**Files:**
- Modify: `/Users/dm3n/Projects/embodied-agency-hypothesis/main.tex`
- Modify: `/Users/dm3n/Projects/embodied-agency-hypothesis/README.md`
- Retain: `/Users/dm3n/Projects/embodied-agency-hypothesis/refs.bib`
- Retain: `/Users/dm3n/Projects/embodied-agency-hypothesis/sources/`

**Interfaces:**
- Consumes: the approved design and existing BibTeX keys.
- Produces: the complete second-edition LaTeX source and matching repository overview.

- [ ] **Step 1: Replace the manuscript narrative**

Rewrite `main.tex` with these sections:

1. `The Claim`
2. `What Manifestation Means`
3. `A Formal Model`
4. `How Vision Enters the Body`
5. `The Body Changes What Is Possible`
6. `Evidence and Boundaries`
7. `Ancient Maps of Transformation`
8. `A Practical Materialization Protocol`
9. `Predictions and Conclusion`

The abstract must state the causal chain in plain language. The formal section must
define visualization `V`, biological state `B`, environment `E`, policy `pi`, and
outcome `Y`.

- [ ] **Step 2: Add the three formal results**

Include:

```text
P(Y | V,B,E) = sum_pi P(Y | do(pi),B,E) P(pi | V,B,E)
```

Prove the mediation theorem by substituting the visualization-independent policy
distribution. Prove reachable-future expansion by set inclusion plus one effective
new policy. Prove repetition amplification using the complement probability
`1 - product_t(1-p_t)`.

- [ ] **Step 3: Add two explanatory figures and the claim audit**

Figure one must show:

```text
vision -> embodied state -> policy -> action -> physical world -> feedback
```

Figure two must show mental, embodied, and physical planes as nested causal layers.

The claim table must classify at least: bioelectric signaling, mental imagery,
implementation intentions, DNA as an antenna, cardiac fields, quantum tunneling,
quantum timeline selection, patent 6,506,148, Gateway, kundalini, and sacred secretion.

- [ ] **Step 4: Write the seven-step protocol**

The protocol must be:

1. Specify the physical target.
2. Visualize the process and identity.
3. Convert vision into implementation intentions.
4. Prepare the body.
5. Design the environment.
6. Act and produce evidence.
7. Measure, learn, and repeat.

- [ ] **Step 5: Rewrite the README**

Update the title, thesis, formal results, evidence boundary, contents, and build
instructions. Do not hard-code page or word counts until Task 2 measures the compiled
artifact.

- [ ] **Step 6: Run source checks**

Run:

```bash
git diff --check
rg -n '—|---|TBD|TODO|FIXME' main.tex README.md
rg -n '^@' refs.bib | wc -l
shasum -a 256 sources/*.pdf
```

Expected: no prohibited writing markers, 56 bibliography records, and unchanged source
hashes.

- [ ] **Step 7: Commit the manuscript rewrite**

```bash
git add main.tex README.md
git commit -m "Rewrite the paper as From Vision to Reality"
```

---

### Task 2: Compile and editorially verify the paper

**Files:**
- Generate: `/Users/dm3n/Projects/embodied-agency-hypothesis/main.pdf`
- Modify: `/Users/dm3n/Projects/embodied-agency-hypothesis/README.md`

**Interfaces:**
- Consumes: the rewritten LaTeX and unchanged bibliography.
- Produces: stable final PDF plus measured page, word, figure, theorem, and citation counts.

- [ ] **Step 1: Compile to a stable PDF**

Run:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

- [ ] **Step 2: Check compiler and text integrity**

Run:

```bash
rg 'undefined|Overfull|Underfull|Warning' main.log
pdfinfo main.pdf
pdftotext main.pdf - | wc -w
pdftotext main.pdf - | rg 'From Vision to Reality|Mediation theorem|Reachable-future theorem|Repetition theorem|Materialization Protocol|Patent 6,506,148|Gateway'
```

Expected: no unresolved citations or references; title and required sections present.

- [ ] **Step 3: Measure and update README**

Record the actual page, extracted-word, cited-reference, figure, formal-result, and
prediction counts in `README.md`.

- [ ] **Step 4: Render and inspect every page**

Run:

```bash
mkdir -p tmp/pdfs/paper
pdftoppm -png -r 150 main.pdf tmp/pdfs/paper/page
```

Create a contact sheet, inspect it, then inspect the title page, every formal-result
page, the claim table, protocol, conclusion, and any dense reference page at original
resolution. Fix and repeat until there are no defects.

- [ ] **Step 5: Recompile after final editorial fixes**

Repeat the stable build and compiler scan. Confirm the final statistics again.

- [ ] **Step 6: Commit the verified artifact**

```bash
git add main.tex main.pdf README.md
git commit -m "Publish From Vision to Reality"
```

---

### Task 3: Replace the Desktop O-1A paper bundle

**Files:**
- Rename: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - The Embodied Agency Hypothesis`
- Create: `/Users/dm3n/Desktop/O-1A/Academic Papers/4 - From Vision to Reality`
- Copy: `main.tex`, `refs.bib`, `README.md`, `main.pdf`, and `sources/`

**Interfaces:**
- Consumes: the verified repository release.
- Produces: the canonical Desktop O-1A paper bundle.

- [ ] **Step 1: Rename the Desktop folder**

Move the existing paper-four folder to `4 - From Vision to Reality`. Keep the Human
Divinity folder at number 5.

- [ ] **Step 2: Replace release files**

Copy repository `main.tex`, `refs.bib`, `README.md`, and `sources/`. Store `main.pdf`
as `From Vision to Reality.pdf`. Remove the old titled PDF from the renamed folder.

- [ ] **Step 3: Verify the bundle**

Run `cmp` for TeX, BibTeX, README, both source PDFs, and the final PDF. Run `pdfinfo`
and `shasum -a 256` on the repository and Desktop PDFs.

---

### Task 4: Update the public O-1A portfolio and itinerary

**Files:**
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/README.md`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/docs/08-o1a-evidence-map.md`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/docs/11-research-embodied-agency.md`
- Modify: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/Daniel_Edgar_Technical_Portfolio.tex`
- Generate: `/Users/dm3n/Projects/daniel-edgar-ai-portfolio/Daniel_Edgar_Technical_Portfolio.pdf`
- Generate: `/Users/dm3n/Desktop/O-1A/Itinerary + portfolio.pdf`

**Interfaces:**
- Consumes: the final title, thesis, measurements, and GitHub location.
- Produces: consistent public portfolio copy and rebuilt O-1A itinerary.

- [ ] **Step 1: Replace all first-edition language**

Use the new title and summarize the three formal results, three-layer model, evidence
boundaries, patent and Gateway treatment, and seven-step protocol. Keep the repository
URL unchanged.

- [ ] **Step 2: Rebuild the portfolio and itinerary**

Run:

```bash
./build-itinerary.sh
```

- [ ] **Step 3: Verify text and layout**

Confirm the technical portfolio is 10 pages, the merged itinerary is 11 pages, and
text extraction contains the new title. Render all itinerary pages and inspect the
full contact sheet plus the paper-entry and repository-index pages.

- [ ] **Step 4: Commit the portfolio release**

```bash
git add README.md docs/08-o1a-evidence-map.md docs/11-research-embodied-agency.md Daniel_Edgar_Technical_Portfolio.tex Daniel_Edgar_Technical_Portfolio.pdf
git commit -m "Update the portfolio for From Vision to Reality"
```

---

### Task 5: Publish and record the second edition

**Files:**
- Modify: `/Users/dm3n/Library/Mobile Documents/iCloud~md~obsidian/Documents/Brain/Memory/project_embodied_agency_hypothesis_paper4.md`

**Interfaces:**
- Consumes: final commits, hashes, measurements, and paths.
- Produces: synchronized public repositories and durable release memory.

- [ ] **Step 1: Push both repositories**

```bash
git -C /Users/dm3n/Projects/embodied-agency-hypothesis push origin main
git -C /Users/dm3n/Projects/daniel-edgar-ai-portfolio push origin main
```

- [ ] **Step 2: Update Brain memory**

Replace first-edition title, metrics, paths, model description, release commits, and
PDF hashes. Preserve the patent and Gateway source hashes and the evidence boundary.

- [ ] **Step 3: Run final verification**

Verify:

- both local HEADs equal `origin/main`;
- both worktrees are clean;
- both GitHub repositories are public;
- repository and Desktop artifacts match;
- source PDFs still match the supplied Downloads files;
- the paper and itinerary have the expected pages and text;
- the final PNG review has no visual defects.
