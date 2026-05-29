# Urban EO/AI evaluation scripts

## What this does

`analyze_model_evaluation.py` reads the **Urban AI Evaluation Workbook** (`Experiment Runs` sheet), then:

- Parses rubric scores (Rubric A: code/execution 0–10, Rubric B: interpretation 0–6)
- Prints validation diagnostics
- Writes summary CSVs to `../results/`
- Generates publication-ready PNG figures

## Input file

By default, the script uses `Urban_AI_Evaluation_Workbook.xlsx` in `evaluations/urban/` (or the first `.xlsx` in that folder if the default file is missing).

Expected workbook structure:

| Sheet | Purpose |
|-------|---------|
| `Experiment Runs` | **Required** — one row per model × task × RAG mode run |
| `Task Suite`, `Rubrics`, `Models`, `Summary` | Reference metadata (not parsed by the script) |

Key columns in `Experiment Runs`: `Model`, `Task ID`, `RAG Mode` (ON/OFF), `Rubric A Total`, `Rubric B Total`, and sub-scores A1–A5, B1–B3.

## How to run

```bash
cd /path/to/sea-scope

# Create env (once)
python -m venv .venv-eval && source .venv-eval/bin/activate
pip install pandas numpy matplotlib openpyxl seaborn

python evaluations/urban/scripts/analyze_model_evaluation.py
```

With an explicit input:

```bash
python evaluations/urban/scripts/analyze_model_evaluation.py \
  --input evaluations/urban/Urban_AI_Evaluation_Workbook.xlsx
```

## Outputs

After a successful run:

- `evaluations/urban/results/model_summary.csv` — per-model aggregates
- `evaluations/urban/results/tier_summary.csv` — per-tier breakdown
- `evaluations/urban/results/task_summary.csv` — per-task detail
- Multiple `.png` figures (mean scores, heatmaps, distributions, sub-rubric breakdown)

When **RAG OFF** rows are scored, the script automatically adds RAG comparison figures (grouped bars, delta charts).
