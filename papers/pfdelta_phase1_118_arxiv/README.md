# PFΔ Phase 1 — arXiv Paper

**Title:** Evolutionary Parameter Adaptation for Streaming Power Flow Robustness  
under Multi-Zone Shocks and N-1 Topology Events  
**Author:** Dumitru Novic, Independent Researcher  
**Target:** arXiv cs.NE (Neural and Evolutionary Computing)  
**Date:** February 2026  

---

## Files

| File | Description |
|------|-------------|
| `main.tex` | Full LaTeX source (self-contained) |
| `references.bib` | BibTeX bibliography (13 references) |
| `figures/` | PDF + PNG figures generated from real experimental data |
| `README.md` | This file |

## Figures

| File | Caption summary |
|------|----------------|
| `fig1_main_comparison.pdf` | S3 convergence, N-1 recovery, PBL — 3 panels with CI95 |
| `fig2_phase_transition.pdf` | Phase transition cliff at nr_max=5/6 |
| `fig3_frozen_comparison.pdf` | Frozen-Elites: S3 convergence + throughput |
| `fig4_ablation.pdf` | Ablation: policy ON/OFF, warm-start ON/OFF |
| `fig5_convergence_timeline.pdf` | Convergence timeline with N-1 shock events |
| `fig6_pareto.pdf` | Pareto frontier: S3 conv vs. iteration cost |

All figures use real experimental metrics from the published test tables
(see `tests/pfdelta_phase1_118/index.html`).

---

## How to Compile

### Requirements
- TeX Live 2022+ or MiKTeX with packages: `geometry`, `amsmath`, `booktabs`,
  `graphicx`, `hyperref`, `natbib`, `caption`, `subcaption`, `algorithm`,
  `algpseudocode`, `enumitem`, `tcolorbox`, `siunitx`, `xcolor`, `microtype`, `parskip`

### Compile (Linux/macOS)

```bash
cd papers/pfdelta_phase1_118_arxiv/
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Or use `latexmk`:

```bash
latexmk -pdf -bibtex main.tex
```

### arXiv Upload

1. Upload `main.tex`, `references.bib`, and all files in `figures/` (PDF versions).
2. Set primary category: **cs.NE** (Neural and Evolutionary Computing).
3. Set secondary category: **cs.SY** (Systems and Control).
4. Recommended keywords: evolutionary computation, power flow, streaming optimisation,
   frozen elites, Newton-Raphson, N-1 contingency, nonlinear surrogate.

---

## Data Provenance

All numerical results in tables and figures are taken directly from:
- **Table A1** (FULL run, 30 seeds): `tests/pfdelta_phase1_118/index.html` §Stage 4
- **Table A2** (Frozen run, 20 seeds): `tests/pfdelta_phase1_118/index.html` §Stage 5

Source data is also published in:
`tests/pfdelta_phase1_118/figures/core_comparison_metrics_source.json`

The research is inspired by the PFΔ benchmark framework:
> Rivera et al., "PFΔ: A Streaming Power Flow Benchmark for Adaptive Solvers",
> arXiv:2510.22048, 2025.
