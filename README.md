# PS2 Exercise 5 — collaboration setup

## Start here

The PS2 setup uses Python 3.13.16, pandas 2.3 series, and a committed
conda-forge Pixi lock file. Four platforms are
resolved: macOS Apple Silicon, macOS Intel, Linux x86-64, and Windows x86-64.
Runtime validation is performed on macOS Apple Silicon; other platforms are
dependency-resolved, not runtime-tested. Install Pixi from https://pixi.sh/ .

From the repository root:

```bash
pixi install --locked -e titanic
pixi run -e titanic jupyter
```

Use the Python kernel from that environment. Do not use a global Python or a
teammate's absolute environment path. Other CPU architectures require a team
manifest/lock update first. See [CONTRIBUTING.md](CONTRIBUTING.md) for branches,
reviews, notebook editing, and local-file rules.

## Files and unfinished coursework

- Existing `Titanic_Data_Journey.ipynb`, `functions/`, and supplied `data/`: preserved from remote main.
- `report.ipynb`: valid EMPTY notebook for the new report, no analysis or text supplied.
- `figures/`: final figures, tracked by Git.
- `pixi.toml` + `pixi.lock`: the shared portable PS2 environment.
- `environment.yml`: retained PS1 defaults-based environment history; it is not the same dependency snapshot as the PS2 Pixi lock. Use Pixi for PS2 collaboration.

Keep the report at 500 words or fewer, excluding graphs. Each chosen visualisation
must justify a feature-selection decision. Review existing figures and favour a
small useful selection. Each author supplies their explanation; the report owner
integrates the final notebook. No feature selections or conclusions are prefilled.


## Setup verification

Verified on 2026-11-03 with Python **3.13.16** and pandas **2.3.3** on
macOS Apple Silicon, using the committed lock file.

- Both notebooks validate; `report.ipynb` remains empty.
- All existing function modules import, and the existing loader reads the supplied CSVs.
- Both existing plotting helpers render PNGs from disposable synthetic data.
- A fresh Jupyter kernel runs a temporary cell and confirms Python 3.13.16 and pandas 2.3.
- Both lock-file environments resolve Python 3.13.16 and pandas 2.3 for all four platforms.

Other platforms were dependency-resolved only, not runtime-tested. No coursework
analysis, answers, model training, or Kaggle data download was performed.

## README maintenance

The original PS1 README is preserved in
[`docs/readme-history/README_PS1_original.md`](docs/readme-history/README_PS1_original.md)
from commit `3929a5a959b1576fabbf3b3257b8367df71711ba`. The README before
Python alignment is preserved in
[`docs/readme-history/README_before_python_alignment.md`](docs/readme-history/README_before_python_alignment.md)
from commit `efdc0d4ea8642c7083a5da975142224445951c03`. Keep these backups unchanged.

When completing the coursework, update this README to explain the selected
visualisations and the reasoning behind feature-selection decisions, and how to
run and export the work. Preserve or restore the original PS1 project overview,
structure, usage instructions, and collaboration guidelines below. The formal
report remains `report.ipynb` (at most 500 words, excluding graphs); the README
does not replace it.

## Original repository instructions (retained)

The following PS1 instructions are preserved unchanged. For PS2 environment
setup, use the current Pixi commands above.

# Titanic Data Journey — D100 Exercise 4

## Project Overview

This project refactors a Jupyter Notebook based on the Kaggle Titanic dataset into a more structured and maintainable Python repository.

The Jupyter Notebook remains the main entry point for presenting the analysis, while reusable functions are organised into separate Python modules.

## Repository Structure

- `Titanic_Data_Journey.ipynb` — Main notebook containing the analysis workflow.
- `functions/` — Reusable Python modules and functions.
- `data/` — Input datasets used in the analysis.
- `configs/` — Project configuration files.
- `outputs/` — Directory for generated outputs.
- `environment.yml` — Conda environment specification.
- `.github/` — GitHub-related project configuration.

## Getting Started

1. Clone the repository to your local computer.
2. Set up a compatible Python environment using the dependencies specified in `environment.yml`. The environment file contains a machine-specific `prefix` path, which may need to be removed or adjusted for your system.
3. Open `Titanic_Data_Journey.ipynb` in VS Code or Jupyter.
4. Select the appropriate Python kernel.
5. Check the dataset paths and run the notebook cells in order.

## Development and Collaboration

The project follows a modular development workflow. Reusable code is organised into Python modules, while the notebook is retained for presenting the analysis.

Contributors should create separate Git branches for their changes, open Pull Requests for review, and merge approved changes into the main branch.
