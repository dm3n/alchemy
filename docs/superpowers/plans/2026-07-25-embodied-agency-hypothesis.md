# The Embodied Agency Hypothesis Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Research, write, compile, verify, publish, and portfolio-integrate Daniel Ray Edgar's fourth independent single-author paper.

**Architecture:** A minimal public LaTeX repository contains the paper, verified bibliography, compiled PDF, reader-facing README, and research design. The paper uses an evidence ladder and an original accessible-futures model to connect bioelectric regulation and embodied cognition to a bounded account of manifestation, with esoteric and Christian material explicitly marked as interpretation.

**Tech Stack:** LaTeX, BibTeX, natbib, TikZ, pgfplots, Poppler, Git, GitHub CLI

## Global Constraints

- Match the established 11-point IMH LaTeX house style.
- Daniel Ray Edgar is the sole author.
- Use no em dashes in authored prose and no AI attribution.
- Prefer primary experiments and authoritative academic sources.
- Do not present unreplicated wave-genetics, quantum-timeline, sacred-secretion, or conspiracy claims as facts.
- Preserve the metaphysical thesis as an explicitly labeled interpretation.
- Publish the repository publicly under `dm3n`.

---

### Task 1: Lock the evidence architecture

**Files:**
- Modify: `docs/superpowers/specs/2026-07-25-embodied-agency-hypothesis-design.md`
- Create: `refs.bib`

**Interfaces:**
- Consumes: the source script, prior papers, and primary-source searches.
- Produces: citation keys and a four-level evidence policy used by `main.tex`.

- [ ] **Step 1: Build the source matrix**

Record primary sources for bioelectricity, magnetocardiography, human cell count,
neural voltage, brain throughput, sleep, circadian alignment, hydration,
inflammation, microbiome, ultraprocessed food, notifications, habits, placebo,
mental imagery, implementation intentions, meditation, quantum biology,
consciousness, kundalini, alchemy, and Christian theosis.

- [ ] **Step 2: Audit the viral claims**

Classify each specific numerical or causal claim as established, supported,
plausible, interpretive, or unsupported. Require a citation adjacent to every
verdict in the paper's claim-audit table.

- [ ] **Step 3: Validate bibliography metadata**

Run:

```sh
rg '^@' refs.bib
rg -n 'doi =|url =' refs.bib
```

Expected: each central scientific source has a resolvable DOI or an authoritative
URL, and every citation key is unique.

- [ ] **Step 4: Commit the research architecture**

```sh
git add docs/superpowers refs.bib
git commit -m "Define the embodied agency research architecture"
```

### Task 2: Draft the full manuscript

**Files:**
- Create: `main.tex`

**Interfaces:**
- Consumes: all citation keys in `refs.bib` and the formal model in the design.
- Produces: a complete, self-contained LaTeX manuscript.

- [ ] **Step 1: Implement the house-style preamble and front matter**

Copy the package, color, theorem, hyperlink, title, author, abstract, and page
setup conventions from `ai-designed-life/main.tex`, changing only paper-specific
commands and metadata.

- [ ] **Step 2: Write the scientific foundation**

Draft the epistemic ladder, bioelectric biology, DNA and neural claim audit, heart
field measurements, quantum-biology boundary, and consciousness evidence.

- [ ] **Step 3: Write the formal contribution**

Define lived reality, enacted future, executable policy set, accessible future set,
and the Embodied Agency Operator. Derive the proposition that intention can change
future distributions only through a causal mediator unless the null physical model
is falsified.

- [ ] **Step 4: Write the biological bandwidth synthesis**

Connect sleep, circadian timing, metabolic state, hydration, inflammation,
microbiome, autonomic regulation, and attention to measured changes in perception
or decision performance.

- [ ] **Step 5: Write the manifestation and incentive sections**

Connect expectation, imagery, implementation intentions, habits, and feedback to
enacted futures. Analyze food and attention markets through documented objective
functions and externalities without asserting an unsupported coordinated plot.

- [ ] **Step 6: Write the interpretive bridge**

Present alchemy, kundalini, theosis, Christ consciousness, and contemplative
practice as symbol systems and phenomenology. State exactly where empirical
anatomy ends and interpretation begins.

- [ ] **Step 7: Add claim audit, predictions, limits, and conclusion**

Include explicit refutation conditions for each prediction and state the strongest
counterarguments to the theory.

### Task 3: Package and verify the paper

**Files:**
- Create: `README.md`
- Create: `main.pdf`

**Interfaces:**
- Consumes: `main.tex` and `refs.bib`.
- Produces: the public paper artifact and reproducible build instructions.

- [ ] **Step 1: Compile**

```sh
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Expected: all commands exit 0.

- [ ] **Step 2: Run textual quality checks**

```sh
! rg -n '—|---' main.tex README.md
! rg -n 'undefined citations|undefined references|Citation .* undefined|Reference .* undefined' main.log
pdftotext main.pdf - | rg 'The Embodied Agency Hypothesis|Falsifiable Predictions|References'
```

Expected: no em dashes, no undefined citations or references, and all major PDF
sections are extractable.

- [ ] **Step 3: Render every page**

```sh
mkdir -p /tmp/embodied-agency-render
pdftoppm -png -r 120 main.pdf /tmp/embodied-agency-render/page
```

Expected: one nonblank PNG per PDF page with no clipped tables, figures, equations,
headers, or bibliography entries.

- [ ] **Step 4: Write the README**

Document the thesis, evidence boundary, formal model, paper structure, source
files, and exact build command.

- [ ] **Step 5: Commit the paper**

```sh
git add main.tex refs.bib main.pdf README.md
git commit -m "Publish The Embodied Agency Hypothesis"
```

### Task 4: Publish and integrate the paper

**Files:**
- Create: `~/Desktop/O-1A/Academic Papers/4 - The Embodied Agency Hypothesis/main.tex`
- Create: `~/Desktop/O-1A/Academic Papers/4 - The Embodied Agency Hypothesis/refs.bib`
- Create: `~/Desktop/O-1A/Academic Papers/4 - The Embodied Agency Hypothesis/README.md`
- Create: `~/Desktop/O-1A/Academic Papers/4 - The Embodied Agency Hypothesis/The Embodied Agency Hypothesis.pdf`
- Modify: `~/Projects/daniel-edgar-ai-portfolio/README.md`
- Modify: `~/Projects/daniel-edgar-ai-portfolio/docs/08-o1a-evidence-map.md`
- Create: `~/Projects/daniel-edgar-ai-portfolio/docs/11-research-embodied-agency.md`
- Modify: `~/Projects/daniel-edgar-ai-portfolio/Daniel_Edgar_Technical_Portfolio.tex`
- Modify: `~/Projects/daniel-edgar-ai-portfolio/Daniel_Edgar_Technical_Portfolio.pdf`
- Modify: `~/Desktop/O-1A/Itinerary + portfolio.pdf`

**Interfaces:**
- Consumes: verified paper artifacts.
- Produces: public GitHub evidence, Desktop O-1A evidence, and rebuilt itinerary.

- [ ] **Step 1: Create and push the public repository**

```sh
gh repo create dm3n/embodied-agency-hypothesis --public --source=. --remote=origin --push
```

Expected: GitHub returns the public repository URL and `main` tracks
`origin/main`.

- [ ] **Step 2: Copy the O-1A evidence bundle**

Create the numbered paper directory, rename the existing Human Divinity manuscript
directory from number 4 to number 5, and copy the four release artifacts. Verify the
repository and Desktop PDFs have identical SHA-256 hashes.

- [ ] **Step 3: Update the portfolio narrative**

Add the fourth paper to the portfolio index, research section, evidence map,
repository list, and at-a-glance narrative. Preserve Human Divinity as a distinct
manuscript.

- [ ] **Step 4: Rebuild the portfolio and itinerary**

```sh
./build-itinerary.sh
```

Expected: the LaTeX portfolio compiles twice and the merged Desktop itinerary
includes the new paper entry.

- [ ] **Step 5: Verify and push portfolio changes**

```sh
git diff --check
git status --short
git add README.md docs/08-o1a-evidence-map.md docs/11-research-embodied-agency.md Daniel_Edgar_Technical_Portfolio.tex Daniel_Edgar_Technical_Portfolio.pdf
git commit -m "Add fourth research paper on embodied agency"
git push origin main
```

Expected: the local and upstream `main` commits match.

### Task 5: Record durable memory

**Files:**
- Create: `Brain/Memory/project_embodied_agency_hypothesis_paper4.md`
- Modify: `Brain/Memory/MEMORY.md`

**Interfaces:**
- Consumes: final repository URLs, PDF page count, paper thesis, verification
  results, and portfolio commit IDs.
- Produces: durable cross-agent context.

- [ ] **Step 1: Write the memory**

Record title, central equation, evidence policy, major claim-audit decisions,
repository, O-1A path, portfolio integration, page count, and commit IDs.

- [ ] **Step 2: Add the index pointer**

Add the new memory under the O-1A papers section in `MEMORY.md`.

- [ ] **Step 3: Run the final release audit**

```sh
git -C ~/Projects/embodied-agency-hypothesis status --short --branch
git -C ~/Projects/daniel-edgar-ai-portfolio status --short --branch
gh repo view dm3n/embodied-agency-hypothesis --json url,visibility,defaultBranchRef
pdfinfo ~/Projects/embodied-agency-hypothesis/main.pdf
pdfinfo ~/Desktop/O-1A/Itinerary\\ +\\ portfolio.pdf
```

Expected: both repositories are clean and synced, the paper repository is public,
and both PDFs report valid metadata and page counts.

