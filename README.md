# Wellbore Flow

`wellflow` is a collection of wellbore and pipe flow calculations for production engineering: single-phase pressure drop (Darcy–Weisbach, Hazen–Williams), two-phase flow (homogeneous mixture, Lockhart–Martinelli, Chisholm), circular and annular conduit geometry, and sand transport (settling velocity, sand transport in conduits).

Fluid properties come from [`resprops`](https://github.com/jshiriyev/reservoir-properties).

---

## Installation

```bash
pip install git+https://github.com/jshiriyev/wellbore-flow.git
```

For development:

```bash
git clone https://github.com/jshiriyev/wellbore-flow.git
cd wellbore-flow
python -m venv .venv
source .venv/bin/activate      # macOS / Linux
.venv\Scripts\activate       # Windows (PowerShell)
pip install -e ".[dev,plots]"
```

The distribution is named `wellbore-flow`; the import name is `wellflow`.

Requirements: `python>=3.10`, `numpy`, `scipy`, `reservoir-properties` (`matplotlib` optional, for plotting)

---

## Package structure

```
wellflow
├── onephase  # single-phase pressure drop (Darcy–Weisbach, Hazen–Williams)
├── twophase  # two-phase flow (mixture, Lockhart–Martinelli, Chisholm)
└── sandy     # sand settling and transport
```

Top-level classes: `Pipe`, `ConduitSlice`, `CircularConduit`, `AnnularConduit`.

---

## Examples

See the notebooks in `docs/`:

* `docs/sand_transportation` — conduit geometry and sand transport demos.
* `docs/well_performance_analysis` — IPR, VLP and pressure traverse notebooks.

---

## Testing

```bash
pytest tests/
```

---

## Contact

* **Javid Shiriyev** — [shiriyevcavid@gmail.com](mailto:shiriyevcavid@gmail.com)
* LinkedIn: [https://www.linkedin.com/in/jshiriyev/](https://www.linkedin.com/in/jshiriyev/)
