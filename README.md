# The Embodied Agency Hypothesis

**Bioelectric Regulation, Cognitive State, and the Construction of Lived Reality**

Daniel Ray Edgar, July 2026

[Read the paper](main.pdf)

## Thesis

The paper develops a bounded, testable account of manifestation.

Human beings do not need to select quantum branches to change the futures they
experience. Intention changes attention and policy selection. Biological state
constrains which policies can be represented and reliably executed. Action changes
the environment, and feedback updates the next cycle. An embodied agent therefore
changes the distribution of reachable futures through ordinary causality.

The paper distinguishes:

- **Ontic reality:** what exists independently of a person's present experience.
- **Lived reality:** the subset of the world perceived, modeled, valued, and
  experienced by an embodied agent.
- **Enacted future:** a later world state whose probability has been changed by the
  agent's actions.

## Formal contribution

For biological state \(B_t\), environment \(E_t\), policy reliability threshold
\(\rho\), and outcome threshold \(\epsilon\), the accessible future set is

```tex
\mathcal{A}_{\epsilon,\rho}(B_t,E_t)
=
\left\{
y:
\exists\pi\in\Pi_{\rho}(B_t,E_t)
\text{ such that }
P(y\mid\operatorname{do}(\pi),B_t,E_t)\ge\epsilon
\right\}.
```

Intention changes the future distribution through policy selection:

```tex
P(Y\mid I_t,B_t,E_t)
=
\sum_{\pi\in\Pi_{\rho}(B_t,E_t)}
P(Y\mid\operatorname{do}(\pi),B_t,E_t)
P(\pi\mid I_t,B_t,E_t).
```

The paper proves two propositions within this model:

1. **Mediator requirement:** when policy and downstream action are fixed, intention
   does not change an external outcome under the ordinary causal graph.
2. **Biological contraction:** when an impaired biological state strictly removes
   executable policies under defined assumptions, its accessible future set contracts.

## Evidence boundary

Every major claim is treated as established, supported, plausible, interpretive, or
unsupported.

The paper supports:

- bioelectric regulation of cells, tissues, and morphogenesis;
- state-dependent effects of sleep, circadian timing, metabolism, hydration,
  inflammation, food environments, and some gut--brain interventions;
- measurable effects of expectation, imagery, implementation intentions, habits,
  notifications, and contemplative practice;
- the monitor-manipulation patent and Gateway memorandum as primary evidence of
  proposed mechanisms and institutional interest;
- manifestation as an embodied loop of intention, attention, policy, action, and
  feedback;
- alchemy, kundalini, theosis, and Christ consciousness as meaningful interpretive
  maps of transformation.

The paper does not present the following as established:

- semantic programming of DNA by ordinary words;
- a privileged three-foot cardiac consciousness field;
- a universal whole-human processing rate;
- depression as quantum decoherence;
- voluntary selection of quantum timelines;
- a patent grant or declassified memorandum as proof of replicated efficacy;
- a coordinated global plot to suppress human divinity;
- a monthly cerebrospinal sacred-secretion cycle.

Molecular quantum effects in biology are real. They do not by themselves demonstrate
a quantum cognitive computer or direct mental control of external events.

## Contents

1. Introduction: Recovering the Signal
2. An Epistemic Ladder: Fact, Model, Metaphor, and Myth
3. The Body Is Bioelectric, but Not Thereby a Quantum Computer
4. The Embodied Agency Hypothesis
5. Biological Bandwidth
6. Manifestation Without Magic
7. Manufactured Interference Without a Master Plot
8. Ancient Symbolic Maps of Transformation
9. Claim Audit
10. Falsifiable Predictions and Proposed Tests
11. Counterarguments, Limits, and Ethical Cautions
12. Conclusion: Becoming the Broadcast

The compiled paper is 26 pages and includes three original figures, a claim-audit
table, two formal propositions, and seven falsifiable predictions.

## Build

Requires a LaTeX distribution with `pdflatex`, BibTeX, TikZ, and the packages named in
`main.tex`.

```sh
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

## Repository contents

- `main.tex`: complete manuscript and original figures
- `refs.bib`: research bibliography with DOI and source metadata
- `main.pdf`: compiled publication
- `sources/`: exact patent and declassified memorandum supplied for documentary audit
- `docs/superpowers/specs/`: research and editorial design
- `docs/superpowers/plans/`: end-to-end publication plan
