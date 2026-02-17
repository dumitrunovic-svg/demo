# ZOR-PFΔ Phase 1 (118-bus) — arXiv Paper

This directory contains the LaTeX source for the Phase 1 paper:

**"ZOR-PFΔ Phase 1: Streaming Power Flow Robustness under Multi-Shocks and N-1 Topology Events (118-bus)"**

## Compilation Instructions

### Prerequisites

- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- Required packages: `amsmath`, `amssymb`, `graphicx`, `booktabs`, `hyperref`, `caption`, `subcaption`, `float`

### Compile

From this directory (`/opt/docs_zor/papers/pfdelta_phase1_118_arxiv/`):

```bash
pdflatex main.tex
pdflatex main.tex  # Run twice for references
```

Or use your preferred LaTeX editor (Overleaf, TeXShop, TeXworks, etc.).

### Output

`main.pdf` — the compiled paper.

## Figures

Figures are located in `figures/` subdirectory. Key plots:

- **S3 convergence comparison** (ZOR vs baselines)
- **Topology shock timeline** (N-1 events + convergence)
- **Converged steps/sec** (Frozen-elites vs ZOR online)
- **Pareto analysis** (nr_max phase transition)

For actual figure files, see artifact paths in `/opt/projects/zor_task_solver/problems/zor_pfdelta_stream_118/`:

- `conf_118_n1_full_once/fairness_a_equal_pf_nr8/*.png`
- `conf_frozen_elites_runtime/*.png`

## Contact

For questions or artifact requests, contact: `contact@inzori.ai`

## License

(Add appropriate license here, e.g., CC-BY-4.0 for paper, MIT for code artifacts)
