# Alchemy

**A Formal Theory of Consciousness, Embodiment, and Materialization**

Daniel Ray Edgar, July 2026

[Read the paper](https://github.com/dm3n/alchemy/blob/main/main.pdf)

## Thesis

Every deliberately created reality exists first as a mental form in the mental/astral
plane. The conscious and embodied human carries that mental form into the physical
plane through identity, policy, action, and feedback.

The paper defines this operation precisely:

> Alchemy is the disciplined process by which a mental form is embodied and enacted
> through a human being, then stabilized as physical reality.

Its causal chain is:

```text
mental form -> embodied human bridge -> policy -> action -> physical reality -> feedback
```

Consciousness does not materialize a desired reality by escaping causality. It
materializes reality by entering causality through a trained body, a coherent identity,
repeated action, and correction by evidence.

## Two planes and the human bridge

- **Mental/Astral Plane:** mental forms, including images, symbols, intentions, goals,
  identities, and possible realities.
- **Physical Plane:** bodies, actions, artifacts, relationships, institutions,
  environments, and observable world states.
- **Human Alchemical Bridge:** consciousness holds the mental form; the body supplies
  state, identity, and skill; policy and action carry it into physical reality;
  feedback returns evidence.

The human being is the alchemical connection between the two planes, not a third plane.

## Formal contribution

For mental form `M`, embodied bridge state `B`, environment `E`, policy `pi`, and
later physical world state `W`, the materialization operator is:

```tex
P(W_{t+1} | M_t,B_t,E_t)
=
\sum_{\pi \in \Pi(B_t,E_t)}
P(W_{t+1} | \operatorname{do}(\pi),B_t,E_t)
P(\pi | M_t,B_t,E_t).
```

The paper proves four results inside the stated model:

1. **Mediation theorem:** if a mental form changes no mediator, it does not change
   an external result under the ordinary causal graph.
2. **Reachable-future theorem:** an embodied state that enables more reliable policies
   can enlarge the set of reachable material futures.
3. **Identity-convergence theorem:** repeated identity-consistent evidence makes an
   enacted identity converge toward its target under a simple update rule.
4. **Repetition theorem:** directed attempts increase the cumulative probability of
   material success.

These are mathematical deductions from explicit assumptions. They are not claims that
thought alone controls shielded external systems.

## The alchemical grammar

```text
solve -> mental form -> embody -> enact -> coagulate -> assay
```

- **Solve:** interrupt an inherited pattern.
- **Mental form:** specify and rehearse the reality to be created.
- **Embody:** prepare the conscious, biological, and psychological bridge.
- **Enact:** apply force through behavior.
- **Coagulate:** stabilize the new pattern in matter, relationship, or institution.
- **Assay:** test the work against evidence and begin again.

## Evidence

The synthesis draws on:

- mental imagery and implementation intentions;
- expectation and placebo physiology;
- identity-based motivation, self-perception, and habit;
- bioelectric signaling and biological pattern regulation;
- sleep, circadian timing, hydration, metabolism, inflammation, and nutrition;
- notifications, attention capture, and environmental design;
- contemplative practice and self-transcendent experience;
- Hermetic alchemy, kundalini, sacred secretion, theosis, and Christ consciousness as
  maps of transformation.

The paper examines the 1983 Army memorandum *Analysis and Assessment of Gateway
Process* as technological alchemy: an attempt to operationalize altered-state
disciplines with audio, feedback, visualization, and staged practice. It also examines
U.S. Patent 6,506,148 B2 as a genuine technical and legal record.

The exact documents are included in `sources/` with SHA-256 hashes. The evidence rule
is explicit: institutional inquiry is not experimental confirmation, and a patent
grant is not independent replication.

## Contents

1. Alchemy Is the Human Operation
2. The Two Planes and the Human Bridge
3. The Human Alchemical Bridge
4. The Mathematics of Materialization
5. Solve et Coagula
6. Inner Alchemy
7. Technological Alchemy
8. The Counter-Alchemical Environment
9. The Great Work
10. Become the Part

The publication is 20 pages with 7,762 extracted words, 56 cited sources, two original
diagrams, four proved theorems, and six falsifiable predictions. It contains no claim
audit table.

## Build

Requires a LaTeX distribution with `pdflatex`, BibTeX, TikZ, and the packages named in
`main.tex`.

```sh
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

## Repository contents

- `main.tex`: complete manuscript, mathematics, and diagrams
- `refs.bib`: bibliography with DOI and source metadata
- `main.pdf`: compiled publication
- `sources/`: exact patent and Gateway PDFs used in the documentary analysis
- `docs/research/`: source and evidence map
- `docs/superpowers/specs/`: editorial and research design
- `docs/superpowers/plans/`: end-to-end publication plan
